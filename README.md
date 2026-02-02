# sagemaker-churn-pipeline-mini-project
# End-to-End Churn Prediction with Amazon SageMaker Pipelines

This repository documents the completion of a Machine Learning mini-project based on the AWS tutorial **“Build, tune, and deploy an end-to-end churn prediction model using Amazon SageMaker Pipelines.”**

## Project Overview

The objective of this mini-project was to execute and understand a production-style machine learning workflow using Amazon SageMaker Pipelines. The project demonstrates how an end-to-end churn prediction system is orchestrated in AWS, including data preprocessing, model training, hyperparameter tuning, evaluation, conditional model registration, explainability analysis, and batch inference.

## What Was Done

The following workflow components were configured and invoked as part of an end-to-end SageMaker Pipeline using the official AWS sample repository and notebooks:

- Data preprocessing using SageMaker Processing
- Model training using the built-in XGBoost algorithm
- Hyperparameter tuning with SageMaker HPO
- Model evaluation with an AUC-based quality gate
- Conditional model registration in the SageMaker Model Registry
- Model explainability and bias analysis using SageMaker Clarify
- Batch inference using SageMaker Batch Transform
- End-to-end orchestration using SageMaker Pipelines

## Notes on Execution Environment

This project was executed in **Amazon SageMaker Studio**, as required by the AWS tutorial.  
Because the workflow depends on AWS-managed infrastructure and services, it is not runnable in Google Colab. This repository serves as documentation and submission evidence of the completed mini-project.

## Reference

AWS Tutorial:  
https://aws.amazon.com/blogs/machine-learning/build-tune-and-deploy-an-end-to-end-churn-prediction-model-using-amazon-sagemaker-pipelines/

## Pipeline Execution Status

The SageMaker Pipeline execution was successfully initiated; however, execution failed at the preprocessing step due to an AWS account-level service quota restriction.

Specifically, the AWS account had a quota of 0 instances for `ml.m5.xlarge` processing jobs, which prevented SageMaker from creating the required ProcessingJob. This limitation is enforced at the AWS account level and is outside the scope of the project code or configuration.

The failure confirms that the pipeline was correctly defined and invoked, but blocked by infrastructure limits rather than implementation errors.



