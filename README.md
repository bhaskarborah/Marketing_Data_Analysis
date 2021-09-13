# Marketing_Data_Analysis

## Create an RDS instance in AWS
For this project, we will create a PostgresSQL database hosted on the cloud of AWS so that every member of the team has access to the same datasets. We first create an RDS instance on AWS, then a PostgresSQL database. After we are all set up on AWS, we connect pgAdmin to the RDS instance we just created.

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

![marketing data table](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi/Screenshots/marketing_data_table_pgAdmin.png)

## Reading from a PostgreSQL table to a pandas DataFrame
- After loading the dataset into our postgres table, we create a pandas dataframe from the 'marketing_data' table in pgAdmin. We follow the below steps: 
 - creating a connection string for the database engine to connect to the database
 - creating a database engine
 - loading data from Postgres table into a panda dataframe to check the communication between Pandas and SQL server.
- Below is a screenshot of the Pandas dataframe:

![mockup database](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi/Screenshots/marketing_df_pd.png)
