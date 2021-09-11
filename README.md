# Marketing_Data_Analysis

UC Berkley Data Visualization Final Project (**Team:** Nhi Nguyen, Vijaya Ayanampudi, Bhaskar Borah, and Scott MacDonald)

## Project Plan and Overview

*Selected topic*

#### Market Segmentation by Demographic Profiles Across Geographic Region

"In marketing, market segmentation is the process of dividing a broad consumer or business market, normally consisting of existing and potential customers, into sub-groups of consumers (known as segments) based on some type of shared characteristics."

[^1]: Wikipedia contributors. (2021, June 23). Market segmentation. In *Wikipedia, The Free Encyclopedia*. Retrieved 14:25, September 11, 2021, from https://en.wikipedia.org/w/index.php?title=Market_segmentation&oldid=1029982660

*Reason the topic was selected*

#### In a very competitive marketplace, companies must optimize their potential addressable market (PAM). Using market segmentation, the benifits are less wasted resources (time and money). It allows the company to target specific potential customers that would most likely turn into actual customers by learning their needs and wants and fulfilling them.

"Market segmentation can help you to define and better understand your target audiences and ideal customers. If you’re a marketer, this allows you to [identify the right market for your products](https://www.lotame.com/finding-target-audience/) and then target your marketing more effectively. Similarly, publishers can use market segmentation to offer more precisely targeted advertising options and to customize their content for different audience groups."

"Market segmentation allows you to target your content to the right people in the right way, rather than targeting your entire audience with a generic message. This helps you increase the chances of people engaging with your ad or content, resulting in more efficient campaigns and improved return on investment (ROI)."

[^2]: *What is market Segmentation? 4 types & 5 benefits*. Lotame. (2021, March 4). Retrieved September 11, 2021, from https://www.lotame.com/what-is-market-segmentation/.2 

*Description of the source of data*

#### The data set chosen was compilied by Dr. Omar Romero-Hernandez and comprises data of 2,240 customers of XYZ company containing

- Customer profiles
- Product preferences
- Campaign successes/failures
- Channel performance

The file is located at https://www.kaggle.com/jackdaoud/marketing-data?select=marketing_data.csv and contains 28 columns of data which are:

| Category            | Description                                                  |
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

*Questions the team hopes to answer with the data*

#### Our team hopes to answer the following questions with the data:

- Which marketing campaign is most successful?
- What does the average customer look like for this company?
- Which products are performing best?
- Which channels are underperforming?

#### Creating a summary of actionable findings to improve advertising campaign success:

- Predict whether or not a customer will respond to the next campaign
- Classify customers into clusters based on their buying behaviors and demographic info

