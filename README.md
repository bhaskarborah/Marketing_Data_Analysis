#   Marketing Data - Analysis

## Overview of Project

XYZ is a company which has an extensive marketing data set. However it has been noted by the Chief Marketing Officer that the recent campaigns of the company have not been as successful as they should be.
The primary objective of this project is analyze the dataset, understand the problem and propose a data-driven solution to eradicate the problem.

## Purpose

Data Segmentation is the process of taking the data you hold and dividing it up and grouping similar data together based on the chosen parameters so that you can use it more efficiently within marketing and operations.

The key benefits of Data Segmentation are:

1. Create messaging that is tailored and sophisticated to suit the needs of the target market – appealing to their needs better.
2. Allows to conduct an analysis of the data stored in the required database, helping to identify potential opportunities and challenges based within it. 
3. Enables us to mass-personalize our marketing communications, reducing costs.
4. Allows us to create a predictive model based on the segmented data for better accuracy in the predictions.

The purpose of the project is defined in the below points:
1. The main objective of this project is to segment the data and train a predictive model which allows the company to maximize the profit of the next marketing campaign.
2. Which marketing campaign is most successful?
3. What does the average customer look like for this company?
4. Which products are performing best?
5. Which channels are under performing?

Provide a data driven solution to fulfill the below objectives and provide a summary of actionable findings to improve advertising campaign success
1. Predict whether or not a customer will respond to the next campaign
2. Classify customers into clusters based on their buying behaviors and demographic info

## Dataset

The dataset consists of 2,240 customers of XYZ company with data on:

Customer profiles
Product preferences
Campaign successes/failures
Channel performance

The source of the dataset is:
https://www.kaggle.com/jackdaoud/marketing-data?select=marketing_data.csv

The column description of the dataset is as below:

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




