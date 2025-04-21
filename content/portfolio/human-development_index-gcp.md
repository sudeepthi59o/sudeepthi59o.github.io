+++
categories = ["cloud"]
coders = []
date = 2025-04-12T23:00:00Z
description = "A Data-Driven Exploration Using GCP and Visualization Tools"
image = "https://ik.imagekit.io/ys4gkaixy/Google-cloud-platform.svg?updatedAt=1744744794909"
title = "Human Development Trends Analysis"
weight=5
type = "post"
[[tech]]
logo = "https://cloud.google.com/images/social-icon-google-cloud-1200-630.png"
name = "Google Cloud Platform (GCP)"
url = "https://cloud.google.com/"
[[tech]]
logo = "https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg"
name = "Python"
url = "https://www.python.org/"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Plotly-logo.png?updatedAt=1745200562355"
name = "Plotly"
url = "https://plotly.com/"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/google-bigquery-logo-1.svg?updatedAt=1745200562438"
name = "BigQuery"
url = "https://cloud.google.com/bigquery"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Google_Cloud_storage.svg?updatedAt=1745200562449"
name = "Cloud Storage"
url = "https://cloud.google.com/storage"
+++

## Overview

This project focuses on analyzing the evolution of global Human Development Indices (HDI), Gender Development Index (GDI), and Gender Inequality Index (GII) over time (1990–2023), using cloud-based data pipelines and interactive visualizations. By investigating the influence of major global crises such as wars, pandemics, and political upheavals, this analysis highlights how significant socio-political events impact human development metrics. The project provides an insightful look at the intersection between global events and human development, offering an effective visualization of these trends to support better decision-making.

----

## Technologies Used

- **Google Cloud Platform (GCP)**: Utilized for creating a scalable, efficient data pipeline using BigQuery and Cloud Functions.
- **BigQuery**: Served as the data storage and querying solution for handling massive datasets. It allowed for high-performance analysis and provided the ability to perform complex queries on the HDI, GDI, and GII data.
- **Python**: Python was used extensively for automating the ETL process, transforming raw data, staging it in BigQuery, and generating visualizations. Custom Python scripts were written to manage data flow and automate repetitive tasks.
- **Plotly**: Used to create dynamic and interactive visualizations of HDI, GDI, and GII trends, enabling users to explore trends across multiple countries and time periods interactively.
- **Cloud Storage**: Employed to store raw datasets securely in GCP buckets, allowing easy retrieval and management of data for further processing.
---

## Background: Understanding Human Development Metrics

The **Human Development Index (HDI)**, developed by the United Nations Development Programme (UNDP), is a key measure of a country’s overall development. Unlike traditional economic indicators, HDI focuses on people and their capabilities, offering a broader view of progress. It combines three core dimensions:

- **Health**: Life expectancy at birth
- **Education**: Mean years of schooling and expected years of schooling
- **Income**: Gross National Income (GNI) per capita, adjusted for purchasing power

While HDI offers a comprehensive overview, it does not fully capture inequalities or environmental impacts. To address these gaps, the UNDP introduced several supplementary indices:

- **Inequality-Adjusted HDI (IHDI)**: Adjusts HDI for inequalities in health, education, and income.
- **Gender Development Index (GDI)**: Highlights gender disparities across HDI dimensions.
- **Gender Inequality Index (GII)**: Measures gender inequality in reproductive health, empowerment, and labor market participation.
- **Multidimensional Poverty Index (MPI)**: Assesses poverty beyond income, focusing on deprivations in health, education, and living standards.
- **Planetary-Adjusted HDI (PHDI)**: Adjusts HDI for environmental sustainability and intergenerational inequality.

These indices provide a more nuanced view of global development, addressing aspects like inequality, gender disparities, poverty, and sustainability that HDI alone cannot fully capture. The UNDP’s Human Development Reports (HDRs) also offer in-depth analyses of global political, economic, and environmental trends, along with detailed insights into how these indices are constructed.

## Project Architecture

High-level data pipeline architecture for HDI analysis project.

![Workflow Diagram](/images/GCP_Workflow.svg)

---

## Project Workflow

### 1. Data Collection

- Datasets from the UNDP Human Development Reports (1990–2023) were collected.
- Data includes key metrics such as HDI, GDI, and GII.

### 2. Data Storage

- Raw CSV files were uploaded to Google Cloud Storage buckets.

### 3. Data Processing

Python scripts were developed to:

- Read the CSV files from Cloud Storage.
- Perform transformations and standardization of raw data.
- Load the cleaned data into BigQuery staging tables for scalable querying and analysis.

```
# Example code snippet for staging tables in BigQuery from Cloud Storage
from google.cloud import bigquery, storage

def create_bigquery_tables(bucket_name, prefix, dataset_id):
    bigquery_client = bigquery.Client()
    storage_client = storage.Client()
    bucket = storage_client.bucket(bucket_name)
    blobs = bucket.list_blobs(prefix=prefix)
    for blob in blobs:
        file_name = blob.name.split("/")[-1]
        if not file_name or not file_name.endswith(".csv"):
            continue
        gcs_uri = f"gs://{bucket_name}/{blob.name}"
        base_name = file_name.split(".")[0]
        parts = base_name.split("-")
        table_id = f"STG_HDI_{parts[-1]}"
        job_config = bigquery.LoadJobConfig(
            autodetect=True,
            source_format=bigquery.SourceFormat.CSV,
            skip_leading_rows=1,
        )
        table_full_id = f"{bigquery_client.project}.{dataset_id}.{table_id}"
        print(f"Creating table {table_full_id} from {gcs_uri}...")
        load_job = bigquery_client.load_table_from_uri(
            gcs_uri, table_full_id, job_config=job_config
        )
        load_job.result()
        print(f"Table {table_full_id} created successfully.") 

```

### 4. Data Analysis

- Views were created in BigQuery to integrate and join the staging tables across multiple years.
- Transformations were applied to align metrics like HDI, GDI, and GII across countries and time periods.
- Analytical queries helped extract trends, such as:
    - HDI improvement rates across continents.
    - Gender disparities over time based on GDI and GII.
    - Impact of historical events (wars, pandemics, etc.) on development indices.

### 5. Data Visualization

Interactive dashboards were created using Plotly to explore global development trends:

- Users can analyze how HDI, GDI, and GII scores evolved over time across different countries.
- Visualizations highlight the impact of global crises, such as wars, pandemics, and political upheavals, on human development metrics.

 Here's an example of how the data is visualized using Plotly:

```
import plotly.express as px

# Example code for creating an interactive plot
def create_interactive_plot(df):
    fig = px.line(df, x='Year', y='HDI', color='Country', title="HDI Trends Over Time")
    fig.show()

# Assuming 'df' is a DataFrame containing HDI data
create_interactive_plot(df)
```

Sample interactive visualization of HDI trends created using Plotly:

### 6. Future Work

- **Automate Pipeline**: Integrate Google Cloud Functions to automate data processing on new uploads.
- **Advanced Analytics**: Leverage BigQuery ML for trend forecasting.
- **Expanded Visualizations**: Build an interactive dashboard application using frameworks such as Dash or Streamlit.
- **Scalability Enhancements**: Optimize BigQuery performance for real-time analytics.

---

### 7. Conclusion
This project demonstrates the integration of cloud technologies like Google Cloud Platform and BigQuery for large-scale data storage, processing, and querying. By automating data processing and utilizing Plotly for visualization, the project effectively analyzes and presents complex datasets related to global development trends.

---

## Resources

- [United Nations Development Programme (UNDP) - Human Development Reports](https://hdr.undp.org/data-center)