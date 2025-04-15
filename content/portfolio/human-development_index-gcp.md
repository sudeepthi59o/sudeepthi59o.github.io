+++
categories = ["cloud"]
coders = ["sudeepthi59o"]
date = 2025-04-12T23:00:00Z
description = "Human Development Trends Analysis"
image = "https://ik.imagekit.io/ys4gkaixy/Google-cloud-platform.svg?updatedAt=1744744794909"
title = "A Data-Driven Exploration Using GCP and Visualization Tools"
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
logo = "https://raw.githubusercontent.com/plotly/marketing-assets/master/logo/plotly-logomark.png"
name = "Plotly"
url = "https://plotly.com/"
[[tech]]
logo = "https://upload.wikimedia.org/wikipedia/commons/2/20/BigQuery_Logo.png"
name = "BigQuery"
url = "https://cloud.google.com/bigquery"
[[tech]]
logo = "https://cloud.google.com/images/products/storage/cloud-storage-icon.svg"
name = "Cloud Storage"
url = "https://cloud.google.com/storage"
+++

### Overview

This project involves analyzing global Human Development Indices (HDI), Gender Development Index (GDI), and Gender Inequality Index (GII) over time using cloud-based data pipelines and interactive visualizations. By analyzing historical trends, it identifies the effects of global crises on development indices, including the Syrian Civil War, Yemen Civil War, and the Taliban's takeover of Afghanistan.

### Technologies Used

- **Google Cloud Platform (GCP)**: Utilized for creating a scalable, efficient data pipeline using BigQuery and Cloud Functions.
- **BigQuery**: Data storage and querying platform used for large-scale, high-performance analysis of HDI, GDI, and GII datasets.
- **Python**: Python scripts were written to automate the process of transforming raw data, staging it in BigQuery, and visualizing trends.
- **Plotly**: Integrated to create interactive and dynamic visualizations to showcase the global development trends.
- **Cloud Storage**: Used for storing and retrieving raw datasets from cloud storage buckets.

### Project Workflow

#### 1. Data Pipeline

- Data is stored in Google Cloud Storage buckets as CSV files.
- Using **Google Cloud Functions**, an event-driven architecture is set up to trigger data processing whenever new files are uploaded.
- **BigQuery** is used for creating tables and querying large datasets.

#### 2. Data Processing

Python scripts are written to automate the transformation and staging of raw data into BigQuery tables. The following Python script automates the process of loading data from Cloud Storage to BigQuery:

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
### 3. Data Visualization

Once the data is processed, the project uses **Plotly** to create interactive visualizations. These visualizations allow users to explore HDI, GDI, and GII trends across different countries over time. Here's an example of how the data is visualized using Plotly:

```
import plotly.express as px

# Example code for creating an interactive plot
def create_interactive_plot(df):
    fig = px.line(df, x='Year', y='HDI', color='Country', title="HDI Trends Over Time")
    fig.show()

# Assuming 'df' is a DataFrame containing HDI data
create_interactive_plot(df)
```

### 4. Challenges Faced

- **Automating Cloud Functions**: Initially, faced difficulties automating the event-driven pipeline, but eventually overcame this by refining Cloud Functions for efficient handling.
- **Data Quality Issues**: Encountered inconsistent data formats and outliers that required additional cleaning before being staged into BigQuery.
- **Looker Studio vs Plotly**: Looker Studio was initially used for visualization but was replaced by Plotly due to better integration with Python and greater customization options.

### 5. Conclusion

This project demonstrates the integration of cloud technologies like Google Cloud Platform and BigQuery for large-scale data storage, processing, and querying. By automating data processing and utilizing Plotly for visualization, the project effectively analyzes and presents complex datasets related to global development trends.
