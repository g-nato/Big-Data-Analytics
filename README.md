
# Big Data Analytics Project: Netflix Content Analysis

## Overview  
This project applies Big Data technologies to analyze Netflix content and develop a scalable solution. It utilizes **Hadoop** and **Spark** for data processing, **MongoDB** as the data warehouse, and **HDFS** for scalable data storage.

## Data  
The dataset used comes from **Kaggle** and contains information about Netflix movie titles. The data, initially in CSV format, is loaded into **HDFS** (Hadoop Distributed File System) for scalable storage and distributed processing.

## Sandbox Environment  
A sandbox environment is created using **Hadoop** and **Spark** for data preprocessing. The data is cleaned and transformed using distributed pipelines and then stored in **MongoDB** for long-term storage and easy access.

## Exploratory Data Analysis (EDA)  
Exploratory Data Analysis (EDA) is performed using standard Python libraries such as **pandas** and **NLTK** to:
- Clean the data (remove stopwords and non-alphanumeric characters).
- Analyze the word distribution in movie titles.
- Select meaningful features for future modeling.

## Model Building  
**Apache Spark** is used to apply analytics and build a classification model on the cleaned dataset. An **undersampling** technique is applied to balance the dataset and improve the model’s performance, addressing **class imbalance** issues.

## MapReduce Jobs  
A **MapReduce** job is implemented to count word occurrences in movie titles. This job consists of two phases:
1. **Map Phase**: The mapper tokenizes movie titles, removes stopwords and non-alphanumeric characters, generating key-value pairs `<word, 1>`.
2. **Reduce Phase**: The reducer aggregates the word occurrences, summing the counts for each word, and stores the result as `<word, count>` pairs in **MongoDB**.

## System Architecture  
The system is structured as follows:
1. **Data Ingestion**: The data is loaded into **HDFS** to enable parallel processing and scalability.
2. **Preprocessing**: Data is cleaned and transformed using **Spark** pipelines.
3. **Analysis and Modeling**: EDA and classification model building are done using **Spark MLlib**.
4. **Storage**: The results are stored in **MongoDB**, which provides scalability for large datasets.

