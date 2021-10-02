# Marketing_Data_Analysis

## Create an RDS instance in AWS
For this project, we create a PostgresSQL database hosted on the cloud of AWS so that every member of the team has access to the same datasets. We first create an RDS instance on AWS, then a PostgresSQL database. After we are all set up on AWS, we connect pgAdmin to the RDS instance we just created.

## pgAdmin Schema
- After creating a pgAdmin server that is connect to our RDS instance, we test the connection by creating a table and load the 'marketing_data.csv' into that table. We run the following query in pgAdmin query tool:
  CREATE TABLE marketing_data (
  ID                      int,
  Year_Birth              int,
  Education              VARCHAR(100),
  Marital_Status         VARCHAR(100),
  Income                VARCHAR(100),
  Kidhome                 int,
  Teenhome                int,
  Dt_Customer            date,
  Recency                 int,
  MntWines                int,
  MntFruits               int,
  MntMeatProducts         int,
  MntFishProducts         int,
  MntSweetProducts        int,
  MntGoldProds            int,
  NumDealsPurchases       int,
  NumWebPurchases         int,
  NumCatalogPurchases     int,
  NumStorePurchases       int,
  NumWebVisitsMonth       int,
  AcceptedCmp3            int,
  AcceptedCmp4            int,
  AcceptedCmp5            int,
  AcceptedCmp1            int,
  AcceptedCmp2            int,
  Response                int,
  Complain                int,
  Country                VARCHAR(40),
  PRIMARY KEY (id)
  );
  
- Next, we import the 'marketing_data.csv' into the 'marketing_data' table. Below is a screenshot of the table after the data has been imported:

![marketing data table](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/Screenshots/marketing_data_table_pgAdmin.png)

## Reading from a PostgreSQL table to a pandas DataFrame
- After loading the dataset into our postgres table, we create a pandas dataframe from the 'marketing_data' table in pgAdmin. We follow the below steps: 
  - creating a connection string for the database engine to connect to the database
  - creating a database engine
  - loading data from Postgres table into a panda dataframe to check the communication between Pandas and SQL server.
- Below is a screenshot of the Pandas dataframe:

![mockup database](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/Screenshots/marketing_df_pd.png)

## Exporting clean marketing_data into the database
- After successfully test the connection between Pandas and our SQL server, we drop the marketing_data table.
- After performing data cleaning and transformation using Pandas library, we follow the above steps to export the marketing_data Pandas DataFrame into a Postgres table stored in our databse.

## Importing country_data.csv into a Postgres table
- We create a table called country_data in pgAdmin and import the country_data.csv into that table.
  -- Create country_data table
  CREATE TABLE country_data (
	  country VARCHAR NOT NULL,
	  lat FLOAT,
	  long FLOAT,
	  per_capita_income FLOAT,
	  currency_conv_to_usd FLOAT,
	  PRIMARY KEY (country)
  );
  
## Creating a subset of marketing_data table
- We create a subset of the marketing_data table and call it demographic_data
  -- Create demographic_data table
  CREATE TABLE demographic_data AS
  SELECT id, year_birth, education, marital_status, 
		  income, kid_home, teen_home, country
  FROM marketing_data;

## Performing a join to create marketing_complete table
- We join marketing_data table with country_data and marketing_data_amounts_total tables into a table called marketing_complete. This table contains 2182 rows and 34 columns.
  -- Create marking_complete table
  SELECT md.*,
	  cd.lat,
	  cd.long,
	  cd.per_capita_income,
	  cd.currency_conv_to_usd,
	  mdat.mnt_sum, 
	  mdat.purchases_sum
  INTO marketing_complete
  FROM marketing_data AS md
	  INNER JOIN country_data AS cd
		  ON (md.country = cd.country)
	  INNER JOIN marketing_data_amounts_total AS mdat
		  ON (md.id = mdat.id);
- Then, we export the marketing_data table into a csv file for future use in data visualization and building machine learning models.

## Create cmp_country table
- We create a Pandas dataset with 9 columns in jupyter notebook containing the number of each campaign’s responder for each country.
- We export the cmp_country dataframe into a csv file stored in the 'Resources' folder.
- We create a table called cmp_country in pgAdmin and import the cmp_country.csv into that table.
  -- Create cmp_country table
  CREATE TABLE cmp_country (
	  country VARCHAR NOT NULL,
	  total_customers INT,
	  cmp1_response FLOAT,
	  cmp2_response FLOAT,
	  cmp3_response FLOAT,
	  cmp4_response FLOAT,
	  cmp5_response FLOAT,
	  cmp6_response FLOAT,
	  cmps_response FLOAT,
	  PRIMARY KEY (country),
	  FOREIGN KEY (country) REFERENCES country_data(country)
  );

## ERD
- Below is an ERD of our database

![ERD](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/marketing_data_ERD.png)

## Demographic Analysis of Campaign Responders
- We divide customers into different groups of age: "<25", "25-35", "35-45", "45-55", "55-65", and ">65".

![age group](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/Screenshots/age_group_binning.png)

- We divide customers into different groups of income: "<10k", "10-35k", "35-55k", "55-75k", "75-90k", "90-120k", and ">120k".

![income group](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/Screenshots/income_group_binning.png)

- We add 2 new columns "Age_Group" and "Income_Group" to the dataset and use this dataset to create visualizations to analyze the demographic of campaign responders. We create a dashboard for each campaign and one for all campaigns.

![all campaign demo](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi-sg2/Demo_Analysis/all_cmps_demo.png)

