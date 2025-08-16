MongoDB Assignment
Overview
This repository contains a Jupyter notebook (Assignment.ipynb) that demonstrates the use of MongoDB and PyMongo to perform data engineering tasks. The notebook addresses a take-home assignment requiring the generation of 10,000 employee documents and the implementation of four specific MongoDB queries to analyze the data. The project uses Python, PyMongo, and the Faker library to generate realistic employee data and execute queries with proper error handling and projections.
The notebook fulfills the following objectives:

Generate 10,000 employee documents with a predefined structure using the Faker library.
Implement four MongoDB queries to filter and project employee data based on specific criteria.
Provide clear comments and explanations for each query.
Ensure robust error handling for all database operations.

This project is submitted as part of a MongoDB learning exercise for Data Engineers.
Prerequisites
To run the notebook, ensure you have the following installed:

MongoDB: A local MongoDB server running on localhost:27017, or a MongoDB Atlas cluster.
Python: Version 3.11 or higher.
Required Python packages:
pymongo: For interacting with MongoDB.
faker: For generating realistic fake data.
python-dateutil: For handling date calculations.


Jupyter Notebook: To execute the .ipynb file.

You can install the required Python packages using:
pip install pymongo faker python-dateutil

Repository Structure

Assignment.ipynb: The main Jupyter notebook containing the code, data generation, and query implementations.
README.md: This file, providing an overview and instructions for the project.

How to Run the Project

Start MongoDB:

Ensure a MongoDB server is running locally on mongodb://localhost:27017/. Alternatively, configure a MongoDB Atlas cluster and update the connection string in the notebook.
To start a local MongoDB server, run:mongod --dbpath /path/to/data




Clone the Repository:
git clone https://github.com/kheus/Assignement-MongoDB.git
cd your-repo-name


Install Dependencies:Run the following command to install the required Python packages:
pip install pymongo faker python-dateutil


Open the Notebook:Launch Jupyter Notebook:
jupyter notebook

Open Assignment.ipynb in your browser.

Execute the Notebook:

Run the cells in order to:
Generate 10,000 employee documents and insert them into the company_db.employees collection.
Execute the four query tasks:
Task 1: High Performers Query (employees with performance rating >= 4.0 and salary > $80,000).
Task 2: Experience-Based Filtering (employees with 5-10 years of experience and salary between $70,000-$120,000).
Task 3: Salary Range Analysis (employees with salary not in $60,000-$100,000).
Task 4: Recent Hires (employees hired in the last 2 years with performance rating > 3.5).




The notebook includes sample outputs for each task, limited to 3 results for readability.



Notebook Contents
1. Data Generation

Generates 10,000 employee documents with fields like employee_id, first_name, last_name, email, department, position, salary, years_experience, performance_rating, skills, hire_date, last_promotion, is_remote, and address.
Uses the Faker library for realistic data and ObjectId for unique document identifiers.
Inserts data into the employees collection in the company_db database.

2. Query Tasks

Task 1: Uses $and, $gte, and $gt operators to filter high-performing employees and projects specific fields.
Task 2: Uses $and, $gte, and $lte to filter employees by experience and salary, projecting contact information.
Task 3: Uses $not with $gte and $lte in an aggregation pipeline to exclude a salary range and create a concatenated full_name.
Task 4: Uses $and, $gte, $gt, $concat, $subtract, and $divide in an aggregation pipeline to find recent hires and calculate tenure_months.

3. Error Handling

Each query function includes try/except blocks to handle potential errors (e.g., connection issues, invalid queries).
Outputs are printed with clear formatting for easy interpretation.

MongoDB Operators Used

Comparison Operators: $gte, $gt, $lte, $not.
Logical Operators: $and.
Aggregation Operators: $match, $project, $concat, $subtract, $divide.
Limit: Used to restrict output to 3 documents for each query.

Submission Details

The notebook is uploaded to this GitHub repository: https://github.com/kheus/Assignement-MongoDB.git.
The notebook and repository link are submitted via the provided Google Form.

Improvements and Future Work

Indexing: Add indexes on frequently queried fields (salary, performance_rating, hire_date) to improve performance:collection.create_index([("salary", 1), ("performance_rating", 1)])
collection.create_index([("hire_date", 1)])


Performance Analysis: Use explain() to analyze query performance.
ETL Integration: Incorporate the queries into an Airflow pipeline for automated data processing.
Testing: Add unit tests to verify query results.
