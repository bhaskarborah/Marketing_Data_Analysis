# Marketing_Data_Analysis
## Create SQL database
The "marketing_data" dataset contains 2240 rows and 28 columns. After loading and transforming the dataset, we save the clean dataframe in a Postgres database for future use. The process of loading this dataset to the Postgres database includes:
- creating a connection string for the database engine to connect to the database
- creating a database engine
- saving the DataFrame to a SQL table using the database engine
- confirming that the table imported correctly in the Postgres databse by running the query 'select count(*) from table_name'

Below is a screenshot of the data table after being saved to the Postgres database:

![mockup database](https://github.com/bhaskarborah/Marketing_Data_Analysis/blob/nhi/postgres_mockup_database.png)
