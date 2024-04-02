# GROUP-6_-ASSIGNMENT-4_DATA-PIPELINE_10-COMPANIES
Generated 100k records for 10 companies by building a data pipeline using Python programming language
## Table of Contents
 
   - [Overview](#overview-1)
   - [Details](#Details-2)
   - [Prerequisites](#Prerequisite-3)
   - [Installation](#Installation-4)
   - [Usage](#Usage-5)
   - [Code](#Code-6)
   - [Acknowledgements](#Acknowledgements-6)
   - [Lead Trainers](#LeadTrainers-7)
   - [Group Members](#GroupMembers-8)
   
## Overview
The Python code was scripted for a data pipeline project that generates synthetic data for 10 companies, with each company having 10,000 records. It utilizes the Faker library to create realistic data and pymysql to interact with a MySQL database. The generated data is ingested into the database through the DataPipeline class, ensuring proper table creation and error handling. This project facilitates the automated generation and storage of large datasets, laying the groundwork for subsequent data analysis and processing tasks. 

## Details 
1. **Data Generation**:
   - The code utilizes the Faker library to generate synthetic data for 10 different companies, each with 10,000 records.
   - Data includes customer IDs, names, addresses, emails, phone numbers, contact preferences, transaction activities, customer preferences, and communication methods.
   - Each company's data is stored in a dictionary where the company name serves as the key and the generated records are stored as values.

2. **Data Ingestion**:
   - The DataPipeline class handles the ingestion of generated data into a MySQL database.
   - It establishes a connection to the MySQL database using pymysql.
   - For each company's data, it creates a corresponding table in the database if it doesn't exist already.
   - It then ingests the generated records into their respective tables.

3. **MySQL Database**:
   - The code assumes the existence of a MySQL database named 'pipeline' with tables for each company's data.
   - Each table has columns corresponding to the fields in the generated data (customer_id, name, address, email, etc.).

4. **Error Handling**:
   - Error handling is implemented to catch exceptions during data ingestion.
   - If an error occurs, it rolls back any changes made to the database and prints an error message.

5. **Main Execution**:
   - In the main section of the code, variables such as database credentials, company names, and the number of records per company are defined.
   - Company data is generated using the generate_company_records function.
   - The DataPipeline class is instantiated with the database credentials, and the run_pipeline method is called to ingest the generated data into the MySQL database.

Overall, the project automates the generation of synthetic data for multiple companies and its ingestion into a MySQL database, providing a basis for further data analysis and processing.
