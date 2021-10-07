#   Marketing Data - Analysis

UC Berkeley Data Visualization Final Project (**Team:** Nhi Nguyen, Vijaya Ayanampudi, Bhaskar Borah, and Scott MacDonald)

Presentation Link: https://docs.google.com/presentation/d/1KhJib9LP4FQ9nTcyoOv1Mo9f-I2zbSNzxyXpxndN51Y/edit#slide=id.gf2ca90ab6f_0_0

The tableau dashboard links:

Dataset Dashboard:
https://public.tableau.com/app/profile/scott.macdonald6291/viz/UCBDataAnalytics-FinalProject/Story1?publish=yes

Campaign Dashboards:
https://public.tableau.com/app/profile/nhi.nguyen1546



## Overview of Project

Sapphire Inc., a company located in Spain with a global footprint, has enlisted the help of four senior analysts to review their demographic and sales data assessing possible trends and opportunities to  increase revenue. 
It has been noted by the Chief Marketing Officer that the recent campaigns of the company have not been as successful as they should be.
The primary objective of this project is analyze the dataset, understand the problem and propose a data-driven solution to eradicate the problem and make a set of recommendations to the company as to which are the most feasible campaigns to launch.

## Purpose

Data Segmentation is the process of taking the data you hold and dividing it up and grouping similar data together based on the chosen parameters so that you can use it more efficiently within marketing and operations.

The key benefits of Data Segmentation are:

1. Create messaging that is tailored and sophisticated to suit the needs of the target market – appealing to their needs better.
2. Allows to conduct an analysis of the data stored in the required database, helping to identify potential opportunities and challenges based within it. 
3. Enables us to mass-personalize our marketing communications, reducing costs.
4. Allows us to create a predictive model based on the segmented data for better accuracy in the predictions.


### Our team hopes to answer the following questions with the data:

- Which marketing campaign is most successful?
- What does the average customer look like for this company?
- Which products are performing the best?
- Which channels are under performing?

### Creating a summary of actionable findings to improve advertising campaign success:

- Predict whether or not a customer will respond to the latest campaign
- Provide suggestions as to which are the most recommended campaigns to launch
- Provide a demographic segmentation of the customer base and advise feasible campaigns based on the demographics of a customer

##  Reason the topic was selected

### In a very competitive marketplace, companies must optimize their potential addressable market (PAM). Using market segmentation, the benefits are less wasted resources (time and money). It allows the company to target specific potential customers that would most likely turn into actual customers by learning their needs and wants and fulfilling them.

"Market segmentation can help you to define and better understand your target audiences and ideal customers. If you’re a marketer, this allows you to [identify the right market for your products](https://www.lotame.com/what-is-market-segmentation/) and then target your marketing more effectively. Similarly, publishers can use market segmentation to offer more precisely targeted advertising options and to customize their content for different audience groups."

"Market segmentation allows you to target your content to the right people in the right way, rather than targeting your entire audience with a generic message. This helps you increase the chances of people engaging with your ad or content, resulting in more efficient campaigns and improved return on investment (ROI)."

[^2]: *What is market Segmentation? 4 types & 5 benefits*. Lotame. (2021, March 4). Retrieved September 11, 2021, from https://www.lotame.com/what-is-market-segmentation/

## Communication Protocol

The team communicated using the below means:

1. A slack channel with the team members has been created where in dataset inputs, EDA suggestions, requirements, details of tasks, action items, code changes, database design etc have been discussed.

2. The team has conducted regular Google meetings to have discussion regarding the progress, requirements and action items of the project.

3. The team has created the below shared directories:
    a. Project Proposals: This link contains the details of the different projects which were considered before deciding on the final one:
    https://docs.google.com/document/d/16pDAf1SeCoWQPkK0wDG6KGJ4e4V19rvHeGtaWDH8FyQ/edit

    b. Shared link to keep track of the required weekly tasks:
    https://docs.google.com/spreadsheets/d/1OOgxBpnZuxi2hHGLxY3LQY5d_HRnzQuFLUDgBpnIdvs/edit#gid=0


## Dataset

The data set chosen was compiled by Dr. Omar Romero-Hernandez and comprises data of 2,240 customers of XYZ company containing

- Customer profiles
- Product preferences
- Campaign successes/failures
- Channel performance

The source of the dataset is:
https://www.kaggle.com/jackdaoud/marketing-data?select=marketing_data.csv

The dataset contains 28 columns of data which are

| Column Name            | Column Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| ID                  | Unique Customer ID                                           |
| Year_Birth          | Customer’s Year of Birth                                     |
| Education           | Customer’s Level of Education                                |
| Marital_Status      | Customer’s Marital Status                                    |
| Income              | Customer’s Yearly Household Income ($USD)                    |
| Kidhome             | Number of Small Children in Customer’s Household             |
| Teenhome            | Number of Teenagers in Customer’s Household                  |
| Dt_Customer         | Date of Customer’s Enrollment with the Company               |
| Recency             | Number of Days Since the Last Purchase                       |
| MntWines            | Amount spent on wine products in the last 2 years            |
| MntFruits           | Amount spent on fruits products in the last 2 years          |
| MntMeatProducts     | Amount spent on meat products in the last 2 years            |
| MntFishProducts     | Amount spent on fish products in the last 2 years            |
| MntSweetProducts    | Amount spent on sweet products in the last 2 years           |
| MntGoldProds        | Amount spent on gold products in the last 2 years            |
| NumDealsPurchases   | Number of purchases made with discount                       |
| NumWebPurchases     | Number of purchases made through company’s web site          |
| NumCatalogPurchases | Number of purchases made using catalogue                     |
| NumStorePurchases   | Number of purchases made directly in stores                  |
| NumWebVisitsMonth   | Number of visits to company’s web site in the last month     |
| AcceptedCmp3        | 1 if customer accepted the offer in the 3rd campaign, 0 otherwise |
| AcceptedCmp4        | 1 if customer accepted the offer in the 4th campaign, 0 otherwise |
| AcceptedCmp5        | 1 if customer accepted the offer in the 5th campaign, 0 otherwise |
| AcceptedCmp1        | 1 if customer accepted the offer in the 1st campaign, 0 otherwise |
| AcceptedCmp2        | 1 if customer accepted the offer in the 2nd campaign, 0 otherwise |
| Response            | 1 if customer accepted the offer in the last campaign, 0 otherwise |
| Complain            | 1 if customer complained in the last 2 years                 |
| Country             | Customer's Location (Country)                                |

## Technology Stack

![Screen Shot 2021-10-03 at 3.09.28 PM](https://i.imgur.com/zD723cE.png)


## Preprocessing the Data

Before initializing any processing on the dataset, we need to perform preprocessing and  Exploratory Data Analysis (EDA) on the dataset.

Below is the dataset read using a dataframe:

![Screen Shot 2021-09-11 at 1.09.29 PM](https://i.imgur.com/1hLYIHB.png)

There are no duplicates in the dataset:
![Screen Shot 2021-09-11 at 1.17.09 PM](https://i.imgur.com/5Wb3DRp.png)

The income field which is a object/string has been cast to float, and white spaces have been removed from the column names:

![Screen Shot 2021-09-11 at 1.18.17 PM](https://i.imgur.com/7TDt1UV.png)


![Screen Shot 2021-09-11 at 1.20.07 PM](https://i.imgur.com/kX3hCj2.png)

![Screen Shot 2021-09-11 at 1.20.13 PM](https://i.imgur.com/1LpWt7I.png)


The Dt_Customer field has been converted from string/object to datetime

![Screen Shot 2021-09-16 at 6.13.00 PM](https://i.imgur.com/quxk9Qz.png)

In the column Marital_Status, there are a few unexpected values:

![Screen Shot 2021-09-16 at 6.14.34 PM](https://i.imgur.com/9bWlIuT.png)

These values are: Alone, Absurd and YOLO

The records with the values of Marital_Status as YOLO and Absurd have been dropped, and Alone has been replaced by Single:

![Screen Shot 2021-09-16 at 6.16.46 PM](https://i.imgur.com/bLpBA4z.png)


There are three records where the Year_Birth is 1900 or less:

![Screen Shot 2021-09-16 at 6.28.36 PM](https://i.imgur.com/uGOPk6y.png)

These three records have been filtered out as we would not be considering them for our modeling or visualization process:

![Screen Shot 2021-09-16 at 6.34.30 PM](https://i.imgur.com/QzdQQsp.png)

The income field has 24 null values. These values might be significant in creation our segments and in our predictive modeling.

![Screen Shot 2021-09-11 at 1.14.01 PM](https://i.imgur.com/KhYpxju.png)

There are 24 records which have the value of Income field as Null. Below are these records:

Out of the 24 records, the Education of 21 Customers is either PHD, Graduation or Master.

We intend to fill up these Null values with the most appropriate values, hence we would be conducting a brief analysis for this purpose.

![Screen Shot 2021-09-16 at 6.38.16 PM](https://i.imgur.com/fZDtIio.png)

The mean the income of the PHD customers is around 56K:

![Screen Shot 2021-09-16 at 6.42.54 PM](https://i.imgur.com/HzouTVP.png)

The mean of the income of the Graduation customers is around 53K:

![Screen Shot 2021-09-16 at 6.44.10 PM](https://i.imgur.com/ct1taDn.png)

The mean of the income of Master customers is also around 53K:

![Screen Shot 2021-09-16 at 6.46.22 PM](https://i.imgur.com/EnPALgw.png)

Below are the mean and median of all the incomes:

![Screen Shot 2021-09-16 at 6.47.34 PM](https://i.imgur.com/mWUw8z6.png)


The mean income is around 52K
The median income is around 51K

Hence it seems that the most appropriate value to use is the mean value.
The reasons are:
1. The mean income of PHD customers is higher than Graduate and Master customers and hence it should be used to fill up al the null values.
2. The mean value of all the incomes, is approximately similar to the mean of customers who are graduates or masters. Hence mean of all incomes would be used to fill up the 24 Null income values.

![Screen Shot 2021-09-16 at 6.52.52 PM](https://i.imgur.com/8ZoZLc2.png)

Now there are no fields which contain any NULL values:

![Screen Shot 2021-09-16 at 6.53.41 PM](https://i.imgur.com/ZXCMdFv.png)

Also, there are records in the dataset which are complete duplicates except the Customer Id/Id:

![Screen Shot 2021-09-16 at 6.55.35 PM](https://i.imgur.com/Ti2Enkd.png)

There are a total of 47 such records.

One of these records has been dropped:

![Screen Shot 2021-09-16 at 6.56.22 PM](https://i.imgur.com/IsRWZ21.png)

Also, there is an income which is way high than the other incomes and does not fall under any range:

![Screen Shot 2021-09-16 at 6.57.41 PM](https://i.imgur.com/MqwIOrs.png)

This record with the extra ordinarily high income has been dropped:

![Screen Shot 2021-09-16 at 7.03.22 PM](https://i.imgur.com/BVdTE5W.png)

The country 'ME' has only three records:

![Screen Shot 2021-09-16 at 7.04.04 PM](https://i.imgur.com/uYnZjHQ.png)

The three records where the country is Montenegro (ME) have been filtered:

![Screen Shot 2021-09-16 at 7.04.50 PM](https://i.imgur.com/BEEka9i.png)

So, we have a total of 2182 records after the preprocessing has been completed.

These 2182 records have been loaded in the marketing_data, in the AWS RDS:

![Screen Shot 2021-09-16 at 7.06.42 PM](https://i.imgur.com/DAjtz6w.png)

The data after being loaded in the table is read as a dataframe:

![Screen Shot 2021-10-03 at 4.37.11 PM](https://i.imgur.com/eT7wc1r.png)

The total number of purchases  and total purchase amounts are calculated and loaded into the Postgres DB:

![Screen Shot 2021-10-03 at 4.38.34 PM](https://i.imgur.com/T6wqgJt.png)

![Screen Shot 2021-10-03 at 4.40.25 PM](https://i.imgur.com/brGaVLL.png)

The Country Demographics are read from a CSV file:

![Screen Shot 2021-10-03 at 4.41.09 PM](https://i.imgur.com/XvWdiLb.png) 

This country demographic details are loaded into the Postgres DB as well:

![Screen Shot 2021-10-03 at 4.42.31 PM](https://i.imgur.com/ibcbYXY.png)

The total number of dependents is calculated by summing up the Kids and Teen Details:
![Screen Shot 2021-10-03 at 4.45.07 PM](https://i.imgur.com/3ldGsYs.png)

The total campaign detail is also calculated by summing up all the campaign details:

![Screen Shot 2021-10-03 at 4.52.10 PM](https://i.imgur.com/hc0LF4D.png)

The age field has been calculated, by subtracting the year of birth from 2014, as the year when this dataset was created is 2014:

![Screen Shot 2021-10-03 at 7.16.57 PM](https://i.imgur.com/uNRVZOv.png)


The field edu_classes with the encoded values for Education has been calculated. This field would be used in the Machine Learning models if required. If not required, then we would not be using in it the ML process

![Screen Shot 2021-10-03 at 5.14.04 PM](https://i.imgur.com/dDAAYCM.png)

The field Marital_Status with the encoded values for Marital Status/Relationship Status has been calculated. This field would be used in the Machine Learning models if required. If not required, then we would not be using in it the ML process

![Screen Shot 2021-10-03 at 5.30.50 PM](https://i.imgur.com/7XVZhDb.png)

The completed dataset is loaded into the marketing_data_complete table in Postgres:

![Screen Shot 2021-10-03 at 5.31.56 PM](https://i.imgur.com/NSGsFp7.png)



## Data Analysis

### The total number of purchases per country:

* Spain has the total number of purchases followed by South Africa


![Screen Shot 2021-09-25 at 4.54.07 PM](https://i.imgur.com/izOcyBh.png)


### The total amount spent per country:

* Customers in Spain spent the most amount of money, followed by customers in South Africa

![Screen Shot 2021-09-25 at 4.55.44 PM](https://i.imgur.com/vMAvfVj.png)

### It can be seen that the total amount purchased decreases with the rise in dependents:

![Screen Shot 2021-09-25 at 5.04.43 PM](https://i.imgur.com/0obtVA2.png)

### It can be seen that the purchase deals increase with the rise in dependents:

![Screen Shot 2021-09-25 at 5.06.25 PM](https://i.imgur.com/ksXLi9C.png)

### The heat map has been created to find out the co-relationship between different fields:

*The High Income Analysis*

* The TotalMnt and all the Mnt Spent/ Mnt Fields are all positively correlated with Income. This means the higher the income, the more the amount people spent.
* The TotalPurchases made and the Number of purchases are positvely correlated to Income

*Dependents Analysis*

* The Income, TotalMnt, Mnt fields, TotalPurchases and the number of purchases are all negatively correlated with Dependents
* The NumDealsPurchases is positively linked with dependents

![Screen Shot 2021-09-25 at 5.08.15 PM](https://i.imgur.com/2sZTKVZ.png)

### The average customer details are as below:

* The average years of birth of a customer is 1969
* The average income of a customer is $52K
* The average number of dependents is 1

![Screen Shot 2021-09-25 at 5.24.28 PM](https://i.imgur.com/JsPBZha.png)

### The average customer number of purchase details are as below:

* The customer accepted less than 1 campaign
* The average total purchases made by a customer is 15
* The worst performing channel is Deals, followed by Catalog
* The best performing channel is Store


![Screen Shot 2021-09-25 at 5.35.32 PM](https://i.imgur.com/mqZ3H8f.png)

### The average customer spending details are as below:

* An average customer spends the least on fruits
* An average customer spends around $26 to 38 on Fruits, Sweet and Fish
* An average customer spends the most on wine which is $304
* An average customer spends around $605 

![Screen Shot 2021-09-25 at 5.48.11 PM](https://i.imgur.com/N6LvvZv.png)

### Campaign Details

* The most successful campaign is the most recent one

![Screen Shot 2021-10-03 at 5.47.55 PM](https://i.imgur.com/nvQjQYK.png)

### Perform analysis on Customers having Dependents or No Dependents

### Customer having no dependents analysis

### The average number of purchase details for a customer having no dependents is as below:
* The customer having no dependents accepted 1 campaign on an average
* The average total number of purchases made by a customer having no dependents is 18
* The worst performing channel is Deals, followed by Catalog
* The best performing channel is Store

![Screen Shot 2021-10-03 at 5.48.54 PM](https://i.imgur.com/c3L97l6.png)

### The average spending for a customer having no dependents is as below:

* An average customer spends the least on fruits
* An average customer spends around $52 to 76 on Fruits, Sweet and Fish
* An average customer spends the most on wine which is $490
* An average customer spends around $110 

![Screen Shot 2021-10-03 at 5.49.35 PM](https://i.imgur.com/imnlp7Q.png)

### The campaign details for a customer having no dependents:

* The most successful campaign is the latest campaign
* The second most successful campaign is Campaign 5

![Screen Shot 2021-10-03 at 5.50.46 PM](https://i.imgur.com/NgfZQ9Y.png)

### Customer having  dependents analysis

### The average number of purchase details for a customer having  dependents is as below:

* The customer having dependents have accepted less than 1 campaign on an average
* The average total number of purchases made by a customer having  dependents is 14
* The worst performing channel is Catalog, followed by Deals
* The best performing channel is Store

![Screen Shot 2021-10-03 at 5.52.10 PM](https://i.imgur.com/7W0rxW8.png)

### The average spending for a customer having dependents is as below:

* An average customer spends the least on fruits
* An average customer spends around $ 16 to 22 on Fruits, Sweet and Fish
* An average customer spends the most on wine which is $230
* An average customer spends around $406 

![Screen Shot 2021-10-03 at 5.52.42 PM](https://i.imgur.com/a5HF8L7.png)

### The campaign details for a customer having dependents:

* The most successful campaign is the latest campaign
* The second most successful campaign is Campaign 3

![Screen Shot 2021-10-03 at 5.54.09 PM](https://i.imgur.com/CEB1eAv.png)

## Database
### Create an RDS instance in AWS
For this project, we will create a PostgresSQL database hosted on the cloud of AWS so that every member of the team has access to the same datasets. We first create an RDS instance on AWS, then a PostgresSQL database. After we are all set up on AWS, we connect pgAdmin to the RDS instance we just created.

### pgAdmin Schema
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

![marketing_data_table_pgAdmin](https://i.imgur.com/79SxYBA.png)

### Reading from a PostgreSQL table to a pandas DataFrame
- The "marketing_data" dataset contains 2240 rows and 28 columns. After loading and transforming the dataset, we save the clean dataframe in a Postgres database for future use. 
- After loading the dataset into our postgres table, we create a pandas dataframe from the 'marketing_data' table in pgAdmin. We follow the below steps: 
  - creating a connection string for the database engine to connect to the database
  - creating a database engine
  - loading data from Postgres table into a panda dataframe to check the communication between Pandas and SQL server.
- Below is a screenshot of the Pandas dataframe:

![marketing_df_pd](https://i.imgur.com/f4gzrfv.png)

### Exporting clean marketing_data into the database
- After successfully test the connection between Pandas and our SQL server, we drop the marketing_data table.
- After performing data cleaning and transformation using Pandas library, we follow the above steps to export the marketing_data Pandas DataFrame into a Postgres table stored in our database.

### Importing country_data.csv into a Postgres table
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

### Creating a subset of marketing_data table
- We create a subset of the marketing_data table and call it demographic_data          

                -- Create demographic_data table
                    CREATE TABLE demographic_data AS
                    SELECT id, year_birth, education, marital_status, 
                        income, kid_home, teen_home, country
                    FROM marketing_data;
          

### Performing a join to create marketing_complete table
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

### Create cmp_country table
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

### Create marketing_data_complete table

- This table contains the complete marketing_data information along with the age, encoded education, relationship values

The Data Definition Language (DDL) statement to create the table is:

            CREATE TABLE marketing_data_complete
            (
                ID bigint,
                Year_Birth bigint,
                Education text ,
                Marital_Status text ,
                Income double precision,
                Kidhome bigint,
                Teenhome bigint,
                Dt_Customer timestamp without time zone,
                Recency bigint,
                MntWines bigint,
                MntFruits bigint,
                MntMeatProducts bigint,
                MntFishProducts bigint,
                MntSweetProducts bigint,
                MntGoldProds bigint,
                NumDealsPurchases bigint,
                NumWebPurchases bigint,
                NumCatalogPurchases bigint,
                NumStorePurchases bigint,
                NumWebVisitsMonth bigint,
                AcceptedCmp3 bigint,
                AcceptedCmp4 bigint,
                AcceptedCmp5 bigint,
                AcceptedCmp1 bigint,
                AcceptedCmp2 bigint,
                Response bigint,
                Complain bigint,
                Country text ,
                mnt_sum bigint,
                purchases_sum bigint,
                Lat bigint,
                Long bigint,
                Per_Capita_Income bigint,
                Currency_Conv_to_USD bigint,
                Total_Dependents          bigint,
              Total_campaigns           bigint,
              age                       bigint,
              edu_classes               bigint,
              relation_status           bigint
            );



### The summary of the tables that we have created is as below:
![Screen Shot 2021-10-03 at 6.16.17 PM](https://i.imgur.com/SyvVxBa.png)


### ERD
- Below is an ERD of our database

![marketing_data_ERD](https://i.imgur.com/DbOUL1W.png)

### Demographic Analysis of Campaign Responders
- We divide customers into different groups of age: "<25", "25-35", "35-45", "45-55", "55-65", and ">65".



![age_group_binning](https://i.imgur.com/5Grv0hX.png)

- We divide customers into different groups of income: "<10k", "10-35k", "35-55k", "55-75k", "75-90k", "90-120k", and ">120k".

![income_group_binning](https://i.imgur.com/GcASwNl.png)

- We add 2 new columns "Age_Group" and "Income_Group" to the dataset and use this dataset to create visualizations to analyze the demographic of campaign responders. We create a dashboard for each campaign and one for all campaigns.


![all_cmps_demo](https://i.imgur.com/cBoo8ni.png)


## Machine Learning

### Connect to the provisional database



![createserver](https://i.imgur.com/r39Axrw.png)

![create_connectiontoaws](https://i.imgur.com/Y0vYU2E.png)




![acessdata](https://i.imgur.com/3BRQJfL.png)

### Initial EDA
To see if overall spending has a linear relationship to the income of the household. From the figure below for linear regression model the overall spending and income seem to have a linear relation.

![LinearRegression](https://i.imgur.com/0XhOavM.png)

### The data is read from the PostgresDB

![Screen Shot 2021-10-03 at 6.18.51 PM](https://i.imgur.com/FO5whZa.png)

### Read the required data for ML

The required columns are read for ML:

![Screen Shot 2021-10-03 at 6.20.06 PM](https://i.imgur.com/4T5TcIG.png)

The features are separated from the target and the data is scaled:

![Screen Shot 2021-10-03 at 6.21.03 PM](https://i.imgur.com/5EXCnPf.png)

The SMOTE model is applied on the dataset:

![Screen Shot 2021-10-03 at 6.22.38 PM](https://i.imgur.com/gZCMAvr.png)

The Random Forest Classifier is applied on the dataset:

![Screen Shot 2021-10-03 at 6.23.16 PM](https://i.imgur.com/NEFwc7d.png)

The SVM classifier is applied on the dataset:

![Screen Shot 2021-10-03 at 6.24.46 PM](https://i.imgur.com/MOs7aNX.png)

The Gradient Boosting Classifier is applied on the dataset:

![Screen Shot 2021-10-03 at 6.25.46 PM](https://i.imgur.com/tdAzQ9c.png)



![Screen Shot 2021-10-03 at 6.26.49 PM](https://i.imgur.com/T7gfkLb.png)

The K Nearest Neighbor Algorithm is applied to the dataset:

![Screen Shot 2021-10-03 at 6.27.18 PM](https://i.imgur.com/EZBxM5B.png)

The Guassian Naive Bayes Classifier is applied to the dataset:

![Screen Shot 2021-10-03 at 6.28.40 PM](https://i.imgur.com/bKMIom1.png)

The Linear Discriminant Analysis model has been applied on the dataset:

![Screen Shot 2021-10-03 at 6.29.32 PM](https://i.imgur.com/TYrpx4n.png)

The logistic regression model has been applied on the dataset:

![Screen Shot 2021-10-03 at 6.31.43 PM](https://i.imgur.com/Bc5t4v8.png)

![Screen Shot 2021-10-03 at 6.33.24 PM](https://i.imgur.com/aS5SOIc.png)

Random oversampling has been applied on the dataset:

![Screen Shot 2021-10-03 at 6.35.34 PM](https://i.imgur.com/E6oCZMa.png)

SMOTE oversampling technique has been applied on the dataset:

![Screen Shot 2021-10-03 at 6.36.15 PM](https://i.imgur.com/bBOl210.png)

SMOTEEN oversampling technique has been applied on the dataset:

![Screen Shot 2021-10-03 at 6.36.57 PM](https://i.imgur.com/puP56fH.png)

K-means clustering has been used to create clusters from this dataset:

![Screen Shot 2021-10-03 at 6.44.55 PM](https://i.imgur.com/ujwVdiB.png)

![Screen Shot 2021-10-03 at 6.46.04 PM](https://i.imgur.com/SrlThwl.png)

Also, agglomerative clustering has been tried as an option to cluster the dataset:

![Screen Shot 2021-10-03 at 6.47.13 PM](https://i.imgur.com/wXL6Wm7.png)

However the clustering using agglomerative clustering has nor been conclusive:

![Screen Shot 2021-10-03 at 6.48.31 PM](https://i.imgur.com/am16t4A.png)

*Hence after undergoing a rigorous process of identifying the best clustering technique and also validating the accuracy of the Machine Learning models, SVM has the greatest accuracy and K-means is the best method to cluster the data*

- SVM:

![Screen Shot 2021-10-03 at 6.24.46 PM](https://i.imgur.com/MOs7aNX.png)

- K means clustering:

![Screen Shot 2021-10-03 at 6.46.04 PM](https://i.imgur.com/SrlThwl.png)

The pros and cons of K-means is as below:

*Pros:*
- Relatively simpler to implement
- Is easily scalable to large datasets
- Easily adapts to new examples

*Cons:*
- It may sometimes cluster outliers
- The value of k has to be chosen manually
- It can be performed on numerical data only


The target customer demographic dashboard:

![Screen Shot 2021-10-06 at 10.12.39 PM](https://i.imgur.com/vcvfBex.png)



### Analysis Results and Conclusions

### Summary of actionable findings to improve advertising campaign success
##### Perform EDA (exploratory data analysis) to determine the various factors for the campaign’s success.

*The EDA performed is described in the section "Preprocessing Data" and "Data Analysis" of this document*


### Which marketing campaign is most successful?

*The most successful campaign is the most recent one*

![Screen Shot 2021-10-03 at 5.47.55 PM](https://i.imgur.com/nvQjQYK.png)

### What does the average customer look like for this company?

*The average customer details are as below:*

* An average customer spends the least on fruits
* An average customer spends around $26 to 38 on Fruits, Sweet and Fish
* An average customer spends the most on wine which is $304
* An average customer spends around $605

![Screen Shot 2021-09-25 at 5.48.11 PM](https://i.imgur.com/N6LvvZv.png)

### Which products are performing best?

*The best performing product is wine*

### Which channels are under performing?

*The under performing channels are deals and catalog purchases (i.e. the average customer made the fewest purchases via these channels)*

### Which channels are best performing?

*The best performing channels are web and store purchases (i.e. the average customer made the most purchases via these channels)*

![Screen Shot 2021-09-25 at 5.35.32 PM](https://i.imgur.com/mqZ3H8f.png)

### Classify customers into clusters based on their buying behaviors and demographic information
- Run a classification algorithm such as k-means to divide the consumers into different clusters based on their buying behaviors and demographic information. This could help in target marketing of a particular product to that particular cluster of consumers.

*SVM has the greatest accuracy and K-means is the best method to cluster the data*

- SVM:

![Screen Shot 2021-10-03 at 6.24.46 PM](https://i.imgur.com/MOs7aNX.png)

- K means clustering:

![Screen Shot 2021-10-03 at 6.46.04 PM](https://i.imgur.com/SrlThwl.png)

### Classifier model to predict whether a customer is a responder or not.

- Predict whether or not a customer will respond to the next campaign.

*Explored the different classification models to check which one is giving a good accuracy in predicting whether a customer is a responder or not to the latest campaign based on the customer's demographic information and buying behaviors* 

*Linear SVM gave a high accuracy of 88%* 

![classifier_accuracy](https://i.imgur.com/thwxHoX.png)

### To train a predictive model which allows the company to maximize the profit of the next marketing campaign
- Define the features and target. Split the data into training set and test set. 
- Run predictive models such as multiple regression to determine the factors for the campaigns' success.

*All of the above questions have been answered/implemented in the "Machine Learning" section of this document*

### Provide suggestions as to which are the most recommended campaigns to launch

* The most successful  campaign was the most recent campaign (column name: Response)


Suggested campaigns:
*Similar campaigns can be conducted for maximizing customer response and revenue generation*

* It has been found that campaign acceptance is positively correlated with income and negatively correlated with having dependents (kids/teenagers)


Suggested campaigns: 
*Create two streams of targeted advertising campaigns:*
*One aimed at high-income individuals without any dependents and another aimed at lower-income individuals with dependents.*

*It can be seen that customers with dependents make the most purchases using deals. A campaign can be launched for customers with dependents including all items, as they do spend less average purchase.*

* The most successful products are wines and meat (i.e. the average customer spent the most on these items)



Suggested campaigns: 
*Launch advertising campaigns on boosting sales of the less popular items*
*Also launch advertising campaigns including better prices for Wine and Meat products for customers with no dependents as they spend more on these items than the average customer*

* The best performing channels are web and store purchases


Suggested campaign: 
*Focus advertising campaigns on the more successful channels, to reach more customers*





