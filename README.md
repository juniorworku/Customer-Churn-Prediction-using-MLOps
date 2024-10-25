# Production-Grade Customer Churn Prediction System

This project demonstrates how to transform a basic customer churn prediction model into a production-grade ML system using modern MLOps practices. The system utilizes Hopsworks for feature store and model registry, implements various pipelines for automation, and provides a Streamlit-based user interface.

## Architecture Overview

The system consists of four main components:
1. Feature Pipeline
2. Training Pipeline
3. Batch Inference Pipeline
4. Streamlit Web Interface

### Technology Stack
- **Feature Store**: Hopsworks
- **Model Registry**: Hopsworks
- **ML Framework**: XGBoost
- **Web Interface**: Streamlit
- **Data Visualization**: Plotly
- **Pipeline Orchestration**: Python-based workflows

## Components Detail

### 1. Feature Pipeline (`churn_feature_pipeline`)
- Handles data ingestion and feature engineering
- Computes and stores feature values in Hopsworks Feature Store
- Ensures feature consistency between training and inference
- Creates feature groups for organized feature management
- Implements feature versioning for reproducibility

### 2. Training Pipeline (`churn_training_pipeline`)
- Retrieves features from Feature Store
- Trains XGBoost classifier model
- Performs model validation and evaluation
- Saves trained model to Hopsworks Model Registry
- Tracks model versions and metadata

### 3. Batch Inference Pipeline (`churn_batch_inference`)
- Fetches latest model from Model Registry
- Loads new customer data for predictions
- Generates batch predictions
- Stores prediction results
- Monitors model performance

### 4. Streamlit Interface (`streamlit_app.py`)
- Provides user-friendly web interface
- Allows real-time prediction requests
- Displays model performance metrics
- Visualizes feature importance
- Shows prediction explanations

## **Getting Started**

### **Prerequisites**
```sh
pip install -r requirements.txt
```

### **Environment Setup**
1. Create a Hopsworks account
2. Set up your project and get API key
3. Configure environment variables:

```sh
export HOPSWORKS_API_KEY='your_api_key'
```

### **Running the System**
1. Feature Pipeline:

```sh
jupyter notebook churn_feature_pipeline.ipynb
```

2. Training Pipeline:

```sh
jupyter notebook churn_training_pipeline.ipynb
```

3. Batch Inference:

```sh
jupyter notebook churn_batch_inference_version2.ipynb
```

4. Web Interface:

```sh
streamlit run streamlit_app.py
```

## **MLOps Best Practices Implemented**

1. Feature Management
    - Centralized feature store
    - Feature versioning
    - Feature validation
    - Automated feature computation

2. Model Management
    - Model versioning
    - Model metadata tracking
    - Model performance monitoring
    - A/B testing capability

3. Data Quality
    - Data validation checks
    - Schema enforcement
    - Data drift detection
    - Feature correlation analysis

4. Monitoring
    - Model performance metrics
    - Prediction drift monitoring
    - Feature drift detection
    - System health checks

5. Reproducibility
    - Version controlled code
    - Tracked model artifacts
    - Reproducible training pipelines
    - Environment management


## **System Improvements Over Basic Implementation**

1. Scalability
    - Batch processing capability
    - Distributed feature computation
    - Efficient data handling
    - Resource optimization
2. Reliability
    - Error handling
    - Pipeline retries
    - Data validation
    - Monitoring alerts
3. Maintainability
    - Modular architecture
    - Clear separation of concerns
    - Documented codebase
    - Version control
4. Operational Excellence
    - Automated workflows
    - Monitoring dashboards
    -Alert systems
    - Performance optimization

## **Future Improvements**

1. Real-time Predictions
    - Implement online inference API
    - Real-time feature serving
    - Low-latency predictions
2. Advanced Monitoring
    - Custom monitoring dashboards
    - Automated alerting system
    - Performance tracking
3. Extended Features
    - Model A/B testing
    - Automated model retraining
    - Feature importance tracking
    - Prediction explanations

## **License**
This project is licensed under the MIT License