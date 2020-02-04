# SalaryPrediction
Salary Prediction Project Based On Job Descriptions (Python)

![alt_text](https://www.kibrissondakika.com/wp-content/uploads/2018/03/doviz-620x320.jpg)

### Project

For this project I will be examining a set of job postings with salaries and then predict salaries for a new set of job postings.

### Data set
we are given three CSV data files:
* train_features.csv: Each row represents metadata for an individual job posting. Has 1000000 rows and 8 Columns

The “jobId” column represents a unique identifier for the job posting. The remaining columns describe features of the job posting.
* train_salaries.csv: Each row associates a “jobId” with a “salary”.
* test_features.csv: Similar to train_features.csv, each row represents metadata for an individual job posting.

The first row of each file contains headers for the columns. Keep in mind that the metadata and salary data may contain errors.

I will be building a model to predict the salaries for the job postings contained in test_features.csv

__Features__  

* <b>jobId :</b> Unique id for each job posting.

* <b>companyId :</b> Represents the Company.

* <b>jobType :</b> Represents individual job type. Such as ECO, manager, Vice_precident, CFO etc.

* <b>degree :</b> Type of degree that an Employee has

* <b>major :</b> Major that employee currently hold

* <b>industry  :</b> Shows the industry to which an employee belong.

* <b>yearsExperience :</b>This difines years of experiences an employee has

* <b>milesFromMetropolis :</b>This indicates how far the job location from the metropliton area.

There are no missing and duplicate values in the dataset.

 ### Please check the notebook for complete analysis of the Data set, including data preprocessing and Exploratory Data Analysis

### Results

#### Baseline model
I have build a baseline model to test different other Machine learning models based on this. My baseline model was built based on average salary for a particular industry. Here I have taken the average salary for that insustry as predicted values and calculated the men square error which was 1367.122.


From the observed results of our baseline model, it was clear that we can definetly improve results.I have developed following models:

* Multiple Linear Regression 
* Random Forest 
* Gradient boosting 

I intended to bring down the MSE to less than 360. Which ever model gives me values closer to my desired values i will have to choose that model.


# Improved Model
GradientBoosting works best for our data. MSE for gradientBoosting model is 364.85. This result is found for default parameters. 

# Feature Importance
Feature importance method is used to find the important features that influences the predictions. Most important features are identified as jobtype, yearsExperience and milefrommetropolices.



