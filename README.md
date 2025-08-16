# MongoDB Assignment

## 📌 Overview
This repository contains a Jupyter notebook (`Assignment.ipynb`) that demonstrates the use of **MongoDB** and **PyMongo** to perform data engineering tasks.  

The notebook addresses a take-home assignment requiring the generation of **10,000 employee documents** and the implementation of **four specific MongoDB queries** to analyze the data.  
It uses **Python, PyMongo, and the Faker library** to generate realistic employee data and execute queries with proper error handling and projections.

### 🎯 Objectives
- Generate **10,000 employee documents** with a predefined structure using the Faker library.  
- Implement **four MongoDB queries** to filter and project employee data based on specific criteria.  
- Provide clear **comments and explanations** for each query.  
- Ensure **robust error handling** for all database operations.  

This project is submitted as part of a **MongoDB learning exercise for Data Engineers**.

---

## ⚙️ Prerequisites
To run the notebook, ensure you have the following installed:

- **MongoDB**: Local server (`localhost:27017`) or a MongoDB Atlas cluster.  
- **Python**: Version 3.11 or higher.  
- Required Python packages:
  - `pymongo` → Interacting with MongoDB  
  - `faker` → Generating realistic fake data  
  - `python-dateutil` → Handling date calculations  
- **Jupyter Notebook** to execute the `.ipynb` file.  

👉 Install dependencies:
```bash
pip install pymongo faker python-dateutil
