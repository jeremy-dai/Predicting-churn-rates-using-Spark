# Predicting-churn-rates-using-Spark

Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data.

This project is part of the Data Scientist Nanodegree program from Udacity, including the following task:
- Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
- Use the machine learning APIs within Spark ML to build and tune models

## Table of Contents
1. [Description](#description)
2. [Files in the repository](#files)
3. [License](#license)

<a name="descripton"></a>
## Description
The full dataset is 12GB. You can choose to deploy a Spark cluster on the cloud using AWS or IBM Cloud to analyze a larger amount of data. Currently the full 12GB dataset is available if you use AWS. If you use IBM, you can download a medium sized dataset to upload to your cluster.

Details on how to do this using AWS or IBM Cloud are included in the last lesson of the Extracurricular Spark Course content linked above. Note that this part is optional, and you will not receive credits to fund your deployment. You can do the IBM portion for free. Using AWS will cost you around $30 if you run a cluster up for a week with the settings we provide.

Once you've built your model, either in the classroom workspace or in the cloud with AWS or IBM, download your notebook and complete the remaining components of your Data Scientist Capstone project, including thorough documentation in a README file in your Github repository, as well as a web app or blog post explaining the technical details of your project. Be sure to review the Project Rubric thoroughly before submitting your project.

Variables:
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


 The project is summarized in this accompanying [post](https://www.linkedin.com/pulse/predicting-churn-rates-spark-yizhen-jeremy-dai).

<a name="files"></a>
## Files in the repository
Using IBM Watson Studio
|- Churn with Spark using IBM cluster.ipynb # Python notebook file of codes for IBM studio
|- Churn with Spark using IBM cluster.html # the html version of the above notebook
Sparkify Project Workspace.ipynb # the exploring on a small sub dataset
figures.pptx # the slides with figures used for the blog
README.md

<a name="license"></a>
## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
