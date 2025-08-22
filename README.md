# MLOps Lifecycle Project

## Overview

Welcome to the MLOps Lifecycle Project! This project showcases the complete journey of machine learning operations (MLOps), from initial experimentation to deployment, using MLflow as our tracking and management tool. It consists of four key files, each representing a different stage in the MLOps workflow.

## Files

### 1. `1st_code_experiment.ipynb`

- **What It Does**: This notebook creates a synthetic imbalanced binary classification dataset. It trains a Logistic Regression model, evaluates its performance using classification metrics, and logs all relevant parameters, metrics, and the trained model to MLflow.
- **Purpose**: The goal here is to establish a baseline experiment with a simple model and learn how to track metrics and models using MLflow.
- **MLOps Connection**: This is where our experiment tracking begins, allowing us to compare different parameter sets in future experiments.

### 2. `2nd_mlflow_binaryclassification.ipynb`

- **What It Does**: In this notebook, we run multiple experiments using different machine learning algorithms, including Logistic Regression, Random Forest, XGBoost, and XGBoost with SMOTETomek to address class imbalance. It prints evaluation metrics for each model.
- **Purpose**: The aim is to compare the performance of various ML algorithms on the same dataset and to see how different techniques for handling class imbalance affect results.
- **MLOps Connection**: This file highlights the importance of experiment management, testing multiple models, and using consistent logging for reproducibility.

### 3. `3rd_mlflow_model_registration.ipynb`

- **What It Does**: This notebook enhances the previous experiments by adding MLflow logging for all models. It tracks hyperparameters, metrics, and models, and registers them in the MLflow Model Registry.
- **Purpose**: The transition from simple experiments to comprehensive experiment tracking and model versioning is crucial for better model governance.
- **MLOps Connection**: This introduces the Model Registry, which is essential for managing model versions before they go into production.

### 4. `mllop_code-1.py`

- **What It Does**: This script uses the real Iris dataset to train Logistic Regression and Random Forest models with intentionally weak configurations (to demonstrate underfitting). It logs metrics, confusion matrices (as images), and models to MLflow, and registers both models in the MLflow Registry.
- **Purpose**: The goal is to demonstrate the complete MLflow cycle: from data preparation to training, evaluation, logging, registration, and loading of models.
- **MLOps Connection**: This serves as a bridge to deployment, ensuring that models are tracked, versioned, and retrievable—key components for continuous integration and deployment (CI/CD) pipelines.

## MLOps Workflow

1. **Experimentation**: Start with a simple dataset and a baseline model, tracking results in MLflow.
2. **Model Comparison**: Experiment with multiple algorithms and techniques, compare their performance, and identify the best candidates.
3. **Experiment Tracking & Registry**: Log models, metrics, and hyperparameters into MLflow, and store models in the Model Registry for version control.
4. **Model Packaging & Loading**: Register models in MLflow and load them from the registry, making them ready for deployment.

## How MLOps Works in This Context

1. **Data & Model Training**: Generate datasets and train models.
2. **Experiment Tracking**: MLflow records metrics, parameters, and artifacts.
3. **Model Registry**: Stores models with versioning to ensure reproducibility.
4. **Deployment Stage**: Models are loaded from the registry and used in production applications.
5. **Monitoring & Iteration**: Although not covered in this project, the next step involves monitoring production models and retraining them if performance drops.

## In Simple Words

This project takes you through the entire MLOps lifecycle—from experimenting with models to comparing algorithms, tracking and registering models, and finally loading them for deployment. It’s a comprehensive guide to understanding how MLOps works in practice!
