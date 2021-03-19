# Predicting-churn-rates-using-Spark

Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data.

This project is part of the Data Scientist Nanodegree program from Udacity, including the following task:
- Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
- Use the machine learning APIs within Spark ML to build and tune models

The project is summarized in this accompanying [post](https://www.linkedin.com/pulse/predicting-churn-rates-spark-yizhen-jeremy-dai).

## Table of Contents
1. [Description](#description)
2. [Files in the repository](#files)
3. [Process](#results)
4. [License](#license)

<a name="descripton"></a>
## Description
We deploy a Spark cluster on the cloud using IBM Cloud to analyze the large amount of data. The data variables are:<br/>
 |-- artist: string (the name of artist)<br/>
 |-- auth: string (the status of log in)<br/>
 |-- firstName: string (the first name of the user)<br/>
 |-- gender: string (the gender of the user)<br/>
 |-- itemInSession: long (number of items in the session)<br/>
 |-- lastName: string (the last name of the user)<br/><br/>
 |-- length: double (the duration of the song)<br/>
 |-- level: string (if the user is a paid one)<br/>
 |-- location: string (the location of the user)<br/>
 |-- method: string (the access method to the app)<br/>
 |-- page: string (the visited page of the app)<br/>
 |-- registration: long (the timestamp of user registration)<br/>
 |-- sessionId: long (the Id of the session)<br/>
 |-- song: string (the name of the song)<br/>
 |-- status: long (the code returned by the app)<br/>
 |-- ts: long (the current timestamp)<br/>
 |-- userAgent: string (related to the data request)<br/>
 |-- userId: string (The Id of the user)

 The libraries used for dependencies are
- pyspark<br/>
- pyspark.sql <br/>
- pyspark.ml<br/>
- datetime<br/>
- pandas<br/>

### Problem Statement
The project aims to predict if a user would leave the music streaming app (i.e. churn) based on the behaviour data. Being able to predict the churn can enable the music app to provide more stimuli to retain the user, such as a discount.

### Metrics
This task falls into the category of the classification problem. Since the churned users are a fairly small subset, the F-1 score is used as the metric to optimize our classifier.

<a name="files"></a>
## Files in the Repository
Using IBM Watson Studio<br/>
|- Churn with Spark using IBM cluster.ipynb # Python notebook file of codes for IBM studio<br/>
|- Churn with Spark using IBM cluster.html # the html version of the above notebook<br/>
Sparkify Project Workspace.ipynb # the exploring on a small sub dataset<br/>
figures.pptx # the slides with figures used for the blog<br/>
README.md

<a name="results"></a>
## Results
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

### Results
Logistic Regression is used as the classifer. The best performer in our case is lambda of 0.01 and alpha of 0.3, which indicates the overfitting is not a serious issue in our model and L2 regularization term plays a more important role than the L1 one.

The features of Logistic Regression models are all standardized so their weight scale indicates their importance in the model. The most important feature is the frequency of visiting each page. Surprisingly, the number of songs as well as gender is set to zero in the model. 


<a name="license"></a>
## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
