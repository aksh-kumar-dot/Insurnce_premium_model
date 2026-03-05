Insurance Premium Risk Prediction API

A Machine Learning powered REST API that predicts an individual's insurance premium risk category based on demographic, lifestyle, and financial attributes.

The application is built using FastAPI for high-performance API serving and Docker for containerized deployment.

Project Overview

Insurance companies determine premium pricing by evaluating various risk factors such as age, lifestyle, income, and occupation.

This project uses a trained machine learning classification model to categorize users into insurance premium risk groups through a REST API.

The system performs feature engineering dynamically and exposes a /predict endpoint that returns the predicted risk category.

Tech Stack

Backend

Python

FastAPI

Machine Learning

Scikit-learn

Pandas

NumPy

Data Validation

Pydantic

Deployment

Docker

Docker Hub

Features

High-performance FastAPI REST API

Automatic feature engineering

Input validation using Pydantic

Computed features:

BMI

Lifestyle Risk

Age Group

City Tier

Machine learning model inference

JSON-based response

Docker containerized deployment

Input Features

The API accepts the following inputs:

Feature	Description
age	Age of the user
weight	Weight in kg
height	Height in meters
income_lpa	Annual income (Lakhs per annum)
smoker	Smoking status (true/false)
city	City of residence
occupation	Employment category
Engineered Features

The API automatically generates additional features before prediction:

BMI

Lifestyle Risk

Age Group

City Tier Classification

These features improve the predictive performance of the ML model.

API Endpoint
POST /predict

Predicts the insurance premium risk category.

Example Request
{
  "age": 35,
  "weight": 75,
  "height": 1.75,
  "income_lpa": 12,
  "smoker": false,
  "city": "Delhi",
  "occupation": "private_job"
}
Example Response
{
  "predicted_category": "medium"
}

Project Structure
insurance-premium-api
│
├── main.py
├── model.pkl
├── requirements.txt
├── Dockerfile
├── README.md

Author

Akash Kumar
B.Tech Computer Science
Machine Learning & Data Science Enthusiast

LinkedIn: https://linkedin.com/in/akash-kumar-1063223ab
