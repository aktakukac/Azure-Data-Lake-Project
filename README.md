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


# Project Solution

## Star Schema Design
A star schema is designed based on the business outcomes listed in the Task Description

_Add ERD diagram image here_

## Data Load
The data was imported into Azure Databricks using Delta Lake to create a Bronze data store

_Add screenshots of data import here_

## Gold Data Store
A gold data store was created in Delta Lake tables using Python notebook

_Add link to Pyton notebook here_

## Star Schema Trasformation
The data was transformed into the star schema for a Gold data store using Python notebook

_Add link to Pyton notebook here_