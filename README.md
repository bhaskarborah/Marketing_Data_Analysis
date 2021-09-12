#   Marketing Data - Analysis

UC Berkeley Data Visualization Final Project (**Team:** Nhi Nguyen, Vijaya Ayanampudi, Bhaskar Borah, and Scott MacDonald)

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

"Market segmentation can help you to define and better understand your target audiences and ideal customers. If you’re a marketer, this allows you to [identify the right market for your products](https://www.lotame.com/finding-target-audience/) and then target your marketing more effectively. Similarly, publishers can use market segmentation to offer more precisely targeted advertising options and to customize their content for different audience groups."

"Market segmentation allows you to target your content to the right people in the right way, rather than targeting your entire audience with a generic message. This helps you increase the chances of people engaging with your ad or content, resulting in more efficient campaigns and improved return on investment (ROI)."

[^2]: *What is market Segmentation? 4 types & 5 benefits*. Lotame. (2021, March 4). Retrieved September 11, 2021, from https://www.lotame.com/what-is-market-segmentation/.2 

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




The income field has 24 null values. These values might be significant in creation our segments and in our predictive modeling.

![Screen Shot 2021-09-11 at 1.14.01 PM](https://i.imgur.com/KhYpxju.png)

This section would be added as we continue with the EDA process.

## Create SQL database
The "marketing_data" dataset contains 2240 rows and 28 columns. After loading and transforming the dataset, we save the clean dataframe in a Postgres database for future use. The process of loading this dataset to the Postgres database includes:
- Creating a connection string for the database engine to connect to the database
- Creating a database engine
- Saving the DataFrame to a SQL table using the database engine
- Confirming that the table imported correctly in the Postgres database by running the query 'select count(*) from table_name'
- Loading data from Postgres table into a panda dataframe to check the communication between Pandas and SQL server.

Below is a screenshot of the data table after being saved to the Postgres database:

![Screen Shot 2021-09-12 at 1.44.18 PM](https://i.imgur.com/v35zfLG.png)

The SQL statement used to create the table is as below:

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


## Machine Learning
#### To train a predictive model which allows the company to maximize the profit of the next marketing campaign
- Define the features and target. Split the data into training set and test set. 
- Run predictive models such as multiple regression to determine the factors for the next campaigns success.
#### Summary of actionable findings to improve advertising campaign success
- Perform EDA(exploratory data analysis) to determine the various factors for the campaign’s success.
- Which products are performing best.
- Which channels are under performing.
- Predict whether or not a customer will respond to the next campaign.
- Based on the data,  predict if a customer will respond to the next campaign or not.
#### Classify customers into clusters based on their buying behaviors and demographic information
- Run a classification algorithm such as k-means to divide the consumers into different clusters based on their buying behaviour and demographic information. This could help in target marketing of a particular product to that particular cluster of consumers.

This section would be updated as we continue to work on the project.





