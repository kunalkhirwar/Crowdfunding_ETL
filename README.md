**INSTRUCTIONS**

The project is divided into the following subsections:

  - Create the Category and Subcategory DataFrames
  - Create the Campaign DataFrame
  - Create the Contacts DataFrame
  - Create the Crowdfunding Database


**Create the Category and Subcategory DataFrames**

1. Extracted and transformed the '*crowdfunding.xlsx*' Excel data to create a **category** DataFrame that has the following columns:
   - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories  
   - A "category" column that contains only the category titles
2. Exported the *category* DataFrame as '*category.csv*'.
3. Extracted and transformed the '*crowdfunding.xlsx*' Excel data to create a **subcategory** DataFrame that has the following columns:
  - A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  - A "subcategory" column that contains only the subcategory titles
4. Exported the *subcategory* DataFrame as '*subcategory.csv*'.


**Create the Campaign DataFrame**

1. Extracted and transformed the '*crowdfunding.xlsx*' Excel data to create a **campaign** DataFrame has the following columns:
    - The "cf_id" column
    - The "contact_id" column
    - The "company_name" column
    - The "blurb" column, renamed to "description"
    - The "goal" column, converted to the float data type
    - The "pledged" column, converted to the float data type
    - The "outcome" column
    - The "backers_count" column
    - The "country" column
    - The "currency" column
    - The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
    - The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
    - The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
    - The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
2. Exported the *campaign* DataFrame as '*campaign.csv*'


**Create the Contacts DataFrame**

1. Chose the option of using **regular expressions** for extracting and transforming the data from the '*contacts.xlsx*' Excel data.
2. Performed the following steps:
   - Imported the '*contacts.xlsx*' file into a DataFrame.
   - Extracted the "contact_id", "name", and "email" columns by using regular expressions.
   - Created a new DataFrame with the extracted data.
   - Converted the "contact_id" column to the integer type.
   - Split each "name" column value into a first and a last name, and placed each in a new column.
   - Cleaned and then exported the DataFrame as '*contacts.csv*'


**Create the Crowdfunding Database**
1. Inspected the four CSV files, and then sketched an ERD of the tables by using **QuickDBD**.
2. Used the information from the ERD to create a table schema for each CSV file.
3. Saved the database schema as a Postgres file named '*crowdfunding_db_schema.sql*'.
4. Created a new Postgres database, named *crowdfunding_db*.
5. Using the database schema, created the tables in the correct order to handle the foreign keys.
6. Verified the table creation by running a SELECT statement for each table.
7. Imported each CSV file into its corresponding SQL table.
8. Verified that each table has the correct data by running a SELECT statement for each.
