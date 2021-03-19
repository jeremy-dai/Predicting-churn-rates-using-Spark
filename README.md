# Predicting-churn-rates-using-Spark

Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data.

This project is part of the Data Scientist Nanodegree program from Udacity, including the following task:
- Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
- Use the machine learning APIs within Spark ML to build and tune models

The project is summarized in this accompanying [post](https://www.linkedin.com/pulse/predicting-churn-rates-spark-yizhen-jeremy-dai).

## Table of Contents
1. [Description](#description)
2. [Files in the repository](#files)
3. [License](#license)

<a name="descripton"></a>
## Description
We deploy a Spark cluster on the cloud using IBM Cloud to analyze the large amount of data. The data variables are:
 |-- artist: string (the name of artist)
 |-- auth: string (the status of log in)
 |-- firstName: string (the first name of the user)
 |-- gender: string (the gender of the user)
 |-- itemInSession: long (number of items in the session)
 |-- lastName: string (the last name of the user)
 |-- length: double (the duration of the song)
 |-- level: string (if the user is a paid one)
 |-- location: string (the location of the user)
 |-- method: string (the access method to the app)
 |-- page: string (the visited page of the app)
 |-- registration: long (the timestamp of user registration)
 |-- sessionId: long (the Id of the session)
 |-- song: string (the name of the song)
 |-- status: long (the code returned by the app)
 |-- ts: long (the current timestamp)
 |-- userAgent: string (related to the data request)
 |-- userId: string (The Id of the user)

### Problem Statement
The project aims to predict if a user would leave the music streaming app (i.e. churn) based on the behaviour data. Being able to predict the churn can enable the music app to provide more stimuli to retain the user, such as a discount.

### Metrics
This task falls into the category of the classification problem. Since the churned users are a fairly small subset, the F-1 score is used as the metric to optimize our classifier.

<a name="files"></a>
## Files in the Repository
Using IBM Watson Studio
|- Churn with Spark using IBM cluster.ipynb # Python notebook file of codes for IBM studio
|- Churn with Spark using IBM cluster.html # the html version of the above notebook
Sparkify Project Workspace.ipynb # the exploring on a small sub dataset
figures.pptx # the slides with figures used for the blog
README.md

### Data Pre-processing
- Handling missing values
- Define churn

### Feature Engineering
- Visiting frequencies per day
- Number of songs between visiting the home page
- Average time spent per session
- Percentage of time spent on different page types 
- Gender
- Whether the user has ever paid

<a name="license"></a>
## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
