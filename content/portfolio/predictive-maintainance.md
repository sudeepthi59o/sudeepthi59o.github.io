+++
categories = ["ai"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Predictive maintainance using AWS"
image = "https://ik.imagekit.io/ys4gkaixy/Amazon_Web_Services_Logo.svg?updatedAt=1744742609304"
title = "Predictive Maintenance Using AWS Machine Learning"
weight=4
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

### **Overview**

This project focuses on building a Predictive Maintenance system using the [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/682/ai4i+2020+predictive+maintenance+dataset) and [AWS SageMaker Canvas](https://aws.amazon.com/sagemaker/canvas/), a no-code ML platform. The goal is to predict machine failures before they occur based on operational and sensor data. By leveraging AWS services, the project efficiently processes and analyzes data to provide real-time predictions of equipment malfunctions.

Key steps included data ingestion, cleaning, feature engineering, exploratory analysis, model building, evaluation, and basic explainability.


### **Technologies Used**
- **AWS Services:**
   - AWS SageMaker Canvas for for low-code/no-code model building
   - AWS Data Wrangler for feature engineering
   - AWS S3 for storage
   - AWS IAM for access management
- **Machine Learning Models:**
  - Logistic Regression
  - Naive Bayes
  - Random Forest
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
- Uploaded the dataset to **AWS S3**.
- Connected **AWS SageMaker Canvas** to the S3 bucket for ingestion.

![Dataset Upload](/images/dataset_to_s3.png)

### 2. Data Preparation
- Used **AWS Data Wrangler** to clean and transform the data.
- Engineered new features where appropriate (e.g., calculating difference between air and process temperatures).
- Dropped ID columns.

![Data Wrangler Flow](/images/data_wrangler_flow.png)

### 3. Exploratory Data Analysis
- Visualized feature correlations and identified significant patterns.
- Made some key observations like:
   - Found that some features (e.g., torque, rotational speed) had significant linear relationships.

![Correlation Heatmap](/images/correlation_features.png)

- Identified early warning patterns:
   - Failures increased sharply when **air temperature** exceeded certain thresholds.

![Air Temperature vs Machine Failure](/images/Variable_AT.png)

   - **Tool Wear** was highly predictive for **Tool Wear Failure**.

![Tool Wear vs Tool Wear Failure](/images/TWF_graphs.png)

### 4. Model Building and Evaluation

- Logistic Regression
   - Chosen as the benchmark model due to the dataset's linear characteristics.
   - Achieved 98%-99% accuracy and high recall across multiple runs.
   - ROC AUC score: 0.98

- Naive Bayes
   - Trained for its simplicity and speed.
   - Achieved similar accuracy (98%-99%) with an average precision of 0.90, effectively handling class imbalance.

- Random Forest
   - Added for its robustness and feature importance insights.
   - Achieved ~97% accuracy.
   - Showed more variance in recall scores across folds.
   - Higher false positives observed, indicating the need for tuning.
   - Provided valuable feature importance analysis.


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
- **Simple models** like **Logistic Regression** can deliver high performance when the data exhibits strong linearity, while **Naive Bayes** can perform well when feature independence assumptions approximately hold — particularly in synthetic datasets with minimal missing values.
- **Feature engineering and exploratory data analysis (EDA)** are essential for successful model building, even when leveraging no-code tools.
- **Cloud-based ML platforms** like AWS SageMaker Canvas accelerate development cycles, enabling rapid prototyping, evaluation, and future deployment at scale.

---

## Future Work
- **Integrate a real-time data ingestion pipeline** to enable continuous monitoring and live failure prediction.
- **Automate deployment** by building SageMaker endpoints for production-ready model serving and API-based access.

---

## External Links
- [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/682/ai4i+2020+predictive+maintenance+dataset)