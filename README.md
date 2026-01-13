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

## Day 4 – Delta Lake & Data Reliability (Unity Catalog) 🚀  
📅 12/01/26

Today I worked on **Delta Lake fundamentals with Unity Catalog**, focusing on how Databricks ensures data reliability, schema enforcement, and safe data ingestion in production environments.

This day was especially insightful because it exposed **real-world constraints and errors** that data engineers face while working with Delta + UC.

---

### 🔍 What I learned:

#### 1️⃣ CSV → Delta Conversion
- Converted raw e-commerce CSV data into **Delta format**
- Understood why Delta is preferred over CSV/Parquet for analytics pipelines

#### 2️⃣ Delta Tables with Unity Catalog
- Created **managed Delta tables** in Unity Catalog
- Learned why `dbfs:/` and `file:/` paths are **not supported in UC**
- Used **Volumes and managed tables** as UC-compliant storage options

#### 3️⃣ Schema Enforcement
- Verified that Delta **rejects invalid schema writes**
- Observed how Delta prevents bad data ingestion at write time
- Understood the difference between schema inference vs schema enforcement

#### 4️⃣ Handling Duplicate Inserts
- Detected duplicate records using business keys
- Implemented de-duplication strategies
- Used **MERGE INTO** for idempotent writes and safe upserts

#### 5️⃣ Practical Debugging (Real Engineering Lessons)
- Resolved:
  - Missing filesystem scheme errors
  - Unity Catalog path restrictions
  - `_c0`, `_c1` column issues caused by missing CSV headers
- Learned why proper schema definition is critical before using MERGE

---

### 🧠 Key Takeaways:
- Delta Lake adds **ACID guarantees** to data lakes
- Unity Catalog enforces **strict governance and storage rules**
- Managed tables are often safer than external locations
- MERGE operations require **clean schemas with correct column names**
- Many Delta errors are not bugs, but **design safeguards**

---

### 🔧 Tech Stack:
- Apache Spark (PySpark)
- Delta Lake
- Databricks Community Edition
- Unity Catalog
- Kaggle E-commerce Behavior Dataset

---

Thanks to the learning initiative by  
@Databricks @Codebasics @indiandataclub  

#DatabricksWithIDC

Day 5 – Delta Lake Advanced Operations (Databricks)
Today’s focus was on managing incremental data, performance optimization, and storage hygiene using Delta Lake. These are critical concepts for building production-grade Lakehouse pipelines.
✅ What I Learned & Implemented
1️⃣ Incremental Data Handling with MERGE
Implemented upserts using Delta Lake MERGE
Efficiently handled new and updated records
Prevented duplicate data during incremental loads
Key use case: CDC pipelines and Bronze → Silver transformations
2️⃣ Querying Historical Data (Time Travel)
Queried previous versions of Delta tables
Used version-based and timestamp-based queries
Understood how Delta maintains transactional history
Useful for auditing, debugging, and rollback scenarios
3️⃣ Performance Optimization with OPTIMIZE
Compacted small files into larger ones
Used Z-Ordering on frequently filtered columns
Improved query latency and scan efficiency
Crucial for large analytical tables
4️⃣ Storage Cleanup with VACUUM
Removed obsolete files created by updates and merges
Learned retention-period best practices
Understood trade-offs between cleanup and time travel
🧠 Key Takeaway
Delta Lake is not just about storing data — it enables reliable incremental processing, auditability, high performance, and efficient storage management, all within the Lakehouse architecture.
🛠️ Tools & Concepts
Databricks Community Edition
Delta Lake
MERGE (Upserts)
Time Travel
OPTIMIZE & Z-ORDER
VACUUM
📌 Building strong foundations for scalable data engineering and analytics pipelines.
#Databricks #DeltaLake #Lakehouse #DataEngineering #BigData #LearningInPublic
