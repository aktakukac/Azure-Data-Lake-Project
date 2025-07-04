# Azure Data Lake Project for Divvy Bikeshare
Udacity Data Engineering Nanodegree Azure Data Lake Project Submission

Created by: __Mihaly Garamvolgyi__

# Task description

## Project Overview
In this project a data lake solution is built for Divvy bikeshare.

Divvy is a bike sharing program in Chicago, Illinois USA that allows riders to purchase a pass at a kiosk or use a mobile application to unlock a bike at stations around the city and use the bike for a specified amount of time. The bikes can be returned to the same station or to another station. The City of Chicago makes the anonymized bike trip data publicly available for projects like this where we can analyze the data.

Since the data from Divvy are anonymous, fake rider and account profiles were generated along with fake payment data to go along with the data from Divvy. The dataset looks like this:

![Original ERD diagram](images/dend-project-erd.jpeg)

The goal of this project is to develop a data lake solution using Azure Databricks using a lake house architecture. 

## Submission Requirements
In the submission:

* A star schema is designed based on the business outcomes listed below
* The data was imported into Azure Databricks using Delta Lake to create a Bronze data store
* A gold data store was created in Delta Lake tables
* The data was transformed into the star schema for a Gold data store

## Business Requirements

#### The business outcomes the solution was designed for are as follows:
* Analyze how much time is spent per ride
* Based on date and time factors such as day of week and time of day
* Based on which station is the starting and / or ending station
* Based on age of the rider at time of the ride
* Based on whether the rider is a member or a casual rider
* Analyze how much money is spent
* Per month, quarter, year
* Per member, based on the age of the rider at account start

#### For extra credit:
* Analyze how much money is spent per member
* Based on how many rides the rider averages per month
* Based on how many minutes the rider spends on a bike per month

## Project Instructions
Technical requirements in submission:

* These requirements were implemented by creating a Python notebook, or notebooks in the Azure Databricks workspace. 
* A PDF of the schema is submitted along with your Azure Databricks notebook files.

## Project Rubric
Dimensional model should have two fact tables (trip and payment)
* Trip table: contains duration and the age of rider at the time of trip
* Payment table: contains payment amount

Dimensional model should have three dimension tables (riders, stations and dates)
* Trip table dimensions: riders, stations and dates
* Payment table dimensions: dates and riders

Extraction step
* Python code to extract information from CSV stored in Databrics
* Write data to the Delta file system
* Spark code using Jupyter Notebooks and Python scripts
* Using DBFS distributed data storage

Load step
* Code should create and load tables from Delta files
* Spark SQL should be used to create and load data

Transform step
* Fact table transformation should contain dimension keys
* Fact tables should match the designed ERD diagram
* Dimension tables should contain the keys but not the facts
* Dimension tables should match the designed ERD diagram
* Spark code in transformation should write to delta, should use overwrite mode and save as a table in delta


# Project Solution

## Star Schema Design
A star schema is designed based on the business outcomes listed in the Task Description

![Final ERD diagram](images/final_ERD.jpg)

## Data Load
A workspace was created in Lab environment using the credentials provided

![Workspace](images/0_workspace_created.jpg)

A compute was created according to the requirements in the Lab environment

![Compute](images/1_compute_created.jpg)

The data was imported into Azure Databricks DBFS using python notebooks

![Files upladed](images/2_upload_files.jpg)

![Files upladed 2](images/2_upload_files_2.jpg)

See: Load_procedure.ipynb

## Bronze Data Store

Data was transformed from csv to delta files

![Bronze](images/3_bronze_delta_tables.jpg)

## Silver Data Store

All data was modified to match the corresponding ERD and loaded to silver delta tables

![Silver](images/4_silver_delta_tables.jpg)

See: Silver_procedure.ipynb

## Star Schema Trasformation
The data was transformed into the star schema for a Gold data store - Fact and Dimension tables were created

![Gold](images/5_gold_delta_tables.jpg)

See: Gold_procedure.ipynb