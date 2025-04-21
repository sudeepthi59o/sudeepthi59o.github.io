+++
categories = ["ai"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Predictive maintainance using AWS"
image = "https://ik.imagekit.io/ys4gkaixy/Amazon_Web_Services_Logo.svg?updatedAt=1744742609304"
title = "Predictive Maintenance Using AWS Machine Learning"
type = "post"
[[tech]]
name = "AWS SageMaker"
url = "https://aws.amazon.com/sagemaker/"
logo = "https://ik.imagekit.io/ys4gkaixy/-yL5MrO-amazon-sagemaker.svg?updatedAt=1745191917808"

[[tech]]
name = "AWS S3"
url = "https://aws.amazon.com/s3/"
logo = "https://ik.imagekit.io/ys4gkaixy/Amazon-S3-Logo.svg?updatedAt=1745191574668"

[[tech]]
name = "AWS IAM"
url = "https://aws.amazon.com/iam/"
logo = "https://ik.imagekit.io/ys4gkaixy/aws-iam.svg?updatedAt=1745191573681"

[[tech]]
name = "Python"
url = "https://www.python.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"

[[tech]]
name = "scikit-learn"
url = "https://scikit-learn.org/"
logo = "https://ik.imagekit.io/ys4gkaixy/Scikit_learn_logo.svg?updatedAt=1745191573114"

[[tech]]
name = "pandas"
url = "https://pandas.pydata.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg"

[[tech]]
name = "numpy"
url = "https://numpy.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg"

[[tech]]
name = "Matplotlib"
url = "https://matplotlib.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg"
+++

## AWS Machine Learning for Predictive Maintenance

### **Overview**

This project focuses on building a Predictive Maintenance system using the [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/682/ai4i+2020+predictive+maintenance+dataset) and [AWS SageMaker Canvas](https://aws.amazon.com/sagemaker/canvas/), a no-code ML platform. The goal is to predict machine failures before they occur based on operational and sensor data. By leveraging AWS services, the project efficiently processes and analyzes data to provide real-time predictions of equipment malfunctions.

Key steps included data ingestion, cleaning, feature engineering, exploratory analysis, model building, evaluation, and basic explainability.


### **Technologies Used**
- **AWS Services:**
   - AWS SageMaker Canvas for automated model building
   - AWS Data Wrangler for feature engineering
   - AWS S3 for storage
   - AWS IAM for access management
- **Machine Learning Models:**
  - Logistic Regression
  - Naive Bayes
  - Random Forest
  - (Explored CNNs and RNNs for future improvements)
- **Programming Language:** Python
- **Libraries/Frameworks:**
  - pandas, numpy, scikit-learn, AWS SDK (boto3)

---

## Dataset
The dataset contains 10,000 samples and 14 columns including:
- **Air temperature [K]**
- **Process temperature [K]**
- **Rotational speed [rpm]**
- **Torque [Nm]**
- **Tool wear [min]**
- **Machine failure** (Target variable - can be 0 or 1)

ID columns like 'UDI' and 'Product ID' were dropped as they were irrelevant for modeling.

---

## Workflow

### 1. Data Ingestion
- Uploaded the dataset to **AWS SageMaker Canvas** and stored in an **S3 bucket**.

![Dataset Upload](/images/dataset_to_s3.png){width=600 height=600}

### 2. Data Preparation
- Used **AWS Data Wrangler** to clean and transform the data.
- Engineered new features where appropriate (e.g., calculating difference between air and process temperatures).
- Dropped ID columns.

![Data Wrangler Flow](/images/data_wrangler_flow.png){width=600 height=600}

### 3. Exploratory Data Analysis
- Visualized feature correlations.
- Found that some features (e.g., torque, rotational speed) had significant linear relationships.

![Correlation Heatmap](/images/correlation_features.png){width=600 height=600}

- Identified early warning patterns:
- Failures increased sharply when **air temperature** exceeded certain thresholds.

![Air Temperature vs Machine Failure](/images/Variable_AT.png){width=600 height=600}

- **Tool Wear** was highly predictive for **Tool Wear Failure**.

![Tool Wear vs Tool Wear Failure](/images/TWF_graphs.png){width=600 height=600}

### 4. Model Building
- Set **Machine Failure** as the prediction target.
- SageMaker Canvas automatically built multiple models including Logistic Regression, Decision Trees, and XGBoost.

### 5. Model Evaluation
- **Logistic Regression** provided a strong baseline with high accuracy and recall.

![Logistic Regression Model Evaluation](/images/LR_model.png){width=600 height=600}

### 6. Model Explainability
- Generated feature importance plots.
- Found that **Torque**, **Rotational Speed**, and **Tool Wear** were critical predictors.

### 7. Deployment
- Although SageMaker Canvas provides easy deployment options, in this project, the model was primarily evaluated offline. 
- In the future, the model can be deployed using **AWS SageMaker Endpoints** for real-time predictions or scheduled batch inference jobs for periodic analysis.

---

### **Impact**
This system enables the prediction machine failures in advance, reducing downtime and maintenance costs. By deploying the model on AWS, the solution is scalable, cost-effective, and capable of handling large datasets.

---

## Key Takeaways
- **SageMaker Canvas** simplifies ML model building for non-coders.
- Proper feature selection significantly improves predictive performance.
- EDA remains a critical step even when using no-code ML tools.
- Predictive maintenance models can reduce downtime and operational costs when deployed properly.

---

## Future Work
- Integrate real-time data pipelines for live failure prediction.
- Deploy the model using SageMaker endpoints for production use.
- Implement deeper interpretability methods (e.g., SHAP values).

---

## External Links
- [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/682/ai4i+2020+predictive+maintenance+dataset)