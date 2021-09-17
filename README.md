#   Marketing Data - Analysis

UC Berkeley Data Visualization Final Project (**Team:** Nhi Nguyen, Vijaya Ayanampudi, Bhaskar Borah, and Scott MacDonald)

Presentation Link: https://docs.google.com/presentation/d/1rXGLG-qk14EAdRtTDJJWhMR-93qbQhRi88W2aqQen0k/edit#slide=id.p

## Overview of Project

XYZ is a company which has an extensive marketing data set. However it has been noted by the Chief Marketing Officer that the recent campaigns of the company have not been as successful as they should be.
The primary objective of this project is analyze the dataset, understand the problem and propose a data-driven solution to eradicate the problem.

## Purpose

"In marketing, market segmentation is the process of dividing a broad consumer or business market, normally consisting of existing and potential customers, into sub-groups of consumers (known as segments) based on some type of shared characteristics."

[^1]: Wikipedia contributors. (2021, June 23). Market segmentation. In *Wikipedia, The Free Encyclopedia*. Retrieved 14:25, September 11, 2021, from https://en.wikipedia.org/w/index.php?title=Market_segmentation&oldid=1029982660

Data Segmentation is the process of taking the data you hold and dividing it up and grouping similar data together based on the chosen parameters so that you can use it more efficiently within marketing and operations.

The key benefits of Data Segmentation are:

1. Create messaging that is tailored and sophisticated to suit the needs of the target market – appealing to their needs better.
2. Allows to conduct an analysis of the data stored in the required database, helping to identify potential opportunities and challenges based within it. 
3. Enables us to mass-personalize our marketing communications, reducing costs.
4. Allows us to create a predictive model based on the segmented data for better accuracy in the predictions.


*Questions the team hopes   to answer with the data*

#### Our team hopes to answer the following questions with the data:

- Which marketing campaign is most successful?
- What does the average customer look like for this company?
- Which products are performing best?
- Which channels are underperforming?

#### Creating a summary of actionable findings to improve advertising campaign success:

- To segment the data and train a predictive model which allows the company to maximize the profit of the next marketing campaign
- Predict whether or not a customer will respond to the next campaign
- Classify customers into clusters based on their buying behaviors and demographic info

##  Reason the topic was selected

#### In a very competitive marketplace, companies must optimize their potential addressable market (PAM). Using market segmentation, the benifits are less wasted resources (time and money). It allows the company to target specific potential customers that would most likely turn into actual customers by learning their needs and wants and fulfilling them.

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



## Preprocessing the Data

Before initializing any processing on the dataset, we need to perform an Exploratory Data Analysis (EDA) on the dataset.

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

Hence it seems that the most appropraite value to use is the mean value.
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


This section would be added as we continue with the EDA process.

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

![marketing_data_table_pgAdmin](https://i.imgur.com/79SxYBA.png)

## Reading from a PostgreSQL table to a pandas DataFrame
- The "marketing_data" dataset contains 2240 rows and 28 columns. After loading and transforming the dataset, we save the clean dataframe in a Postgres database for future use. 
- After loading the dataset into our postgres table, we create a pandas dataframe from the 'marketing_data' table in pgAdmin. We follow the below steps: 
  - creating a connection string for the database engine to connect to the database
  - creating a database engine
  - loading data from Postgres table into a panda dataframe to check the communication between Pandas and SQL server.
- Below is a screenshot of the Pandas dataframe:

![marketing_df_pd](https://i.imgur.com/f4gzrfv.png)

## Machine Learning

#### Connect to the provisional database



![createserver](https://i.imgur.com/r39Axrw.png)

![create_connectiontoaws](https://i.imgur.com/Y0vYU2E.png)




![acessdata](https://i.imgur.com/3BRQJfL.png)

#### Initial EDA
To see if overall spending has a linear relationship to the income of the household. From the figure below for linear regression model the overall spending and income seem to have a linear relation.

![LinearRegression](https://i.imgur.com/0XhOavM.png)


### Future Analysis

#### To train a predictive model which allows the company to maximize the profit of the next marketing campaign
- Define the features and target. Split the data into training set and test set. 
- Run predictive models such as multiple regression to determine the factors for the next campaigns success.
#### Summary of actionable findings to improve advertising campaign success
- Perform EDA(exploratory data analysis) to determine the various factors for the campaign’s success.
- Which products are performing best.
- Which channels are underperforming.
- Predict whether or not a customer will respond to the next campaign.
- Based on the data,  predict if a customer will respond to the next campaign or not.
#### Classify customers into clusters based on their buying behaviors and demographic information
- Run a classification algorithm such as k-means to divide the consumers into different clusters based on their buying behaviours and demographic information. This could help in target marketing of a particular product to that particular cluster of consumers.

This section would be updated as we continue to work on the project.





