# Databricks-challenge
# Databricks Learning Journey – Day 1

**Date:** 09/01/2026  

## Overview
This repository documents my learning journey with **Databricks and PySpark**, focusing on understanding modern data engineering platforms through hands-on practice.

---

## Day 1: Platform Setup & First Steps

### Topics Learned
- Why Databricks compared to Pandas and Hadoop  
- Fundamentals of Lakehouse architecture  
- Databricks workspace structure (Workspace, Compute, Data Explorer)  
- Industry use cases (Netflix, Shell, Comcast)  

---

## Hands-on Tasks Completed
1. Created a Databricks Community Edition account  
2. Explored Workspace, Compute, and Data Explorer  
3. Created the first Databricks notebook  
4. Executed basic PySpark commands  

---
Key Takeaways
Databricks provides an integrated Lakehouse platform combining data engineering and analytics
PySpark enables scalable data transformations using lazy evaluation
Databricks notebooks offer an interactive and efficient development environment
Tools & Technologies
Databricks Community Edition
PySpark
Learning References & Acknowledgements
This learning initiative is supported by the data community and learning resources from:
Databricks — https://www.databricks.com
Codebasics — https://www.codebasics.io
Indian Data Club — https://indiandataclub.com

## Day 2 – Apache Spark Fundamentals 🚀

Today I explored the fundamentals of Apache Spark using Databricks Community Edition.

### What I learned:
- Spark architecture (Driver, Executors, DAG)
- Difference between DataFrames and RDDs
- Lazy evaluation in Spark
- Using Databricks magic commands (%python, %sql, %fs)

### What I built:
- Loaded an e-commerce CSV dataset into Spark
- Performed select, filter, groupBy, and orderBy operations
- Aggregated revenue by product category
- Exported processed data back to storage

Apache Spark makes large-scale data processing both powerful and intuitive when using DataFrames.

Thanks to the learning initiative by @Databricks, @Codebasics, and @indiandataclub 🙌  
#DatabricksWithIDC

## Day 3 – Advanced Spark Analytics 🚀  
📅 11/01/26

Today I moved beyond basic Spark operations and worked on **advanced analytics patterns used in real-world data engineering and analytics workflows**.

### 🔍 What I learned:
- Performing **complex joins** between raw event data and aggregated metrics
- Using **window functions** to calculate running totals
- Creating **derived features** for analytics and ML use cases
- Understanding how Spark optimizes these operations using DAGs and lazy evaluation

---

### 🛠️ What I implemented:

#### 1️⃣ Complex Joins
- Joined raw user activity data with user-level purchase aggregates  
- Used LEFT JOINs to preserve non-purchasing users  
- Typical use case: customer analytics and behavioral segmentation

#### 2️⃣ Window Functions
- Calculated **running (cumulative) spend per user over time**
- Used `partitionBy` and `orderBy` to track user-level temporal behavior  
- Common in churn analysis, fraud detection, and growth analytics

#### 3️⃣ Derived Features
Engineered meaningful features such as:
- Total spend per user  
- Average spend per purchase  
- High-value user flag  
- Price bucket classification (LOW / MEDIUM / HIGH)

These features are directly usable for:
- Dashboards
- Business insights
- Downstream ML models

---

### ✅ Key Takeaways:
- Spark window functions enable powerful time-based analytics at scale
- Feature engineering is a critical step between raw data and ML
- DataFrames provide both performance and readability for complex logic
- Spark transformations remain lazy until an action is triggered

---

### 🔧 Tech Stack:
- Apache Spark (PySpark)
- Databricks Community Edition
- Kaggle E-commerce Dataset

Thanks to the learning initiative by  
@Databricks @Codebasics @indiandataclub  

#DatabricksWithIDC
