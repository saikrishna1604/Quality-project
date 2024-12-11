Data-analyst-vinuthna
Portfolio Part 1
Project Title: “Data Analytics for the City of Vancouver: Unlocking Urban Insights Using AWS Cloud Solutions”

Objective The aim is to design and implement a Data Analytics Platform (DAP) to analyze and visualize the geographic distribution of VAHEF (Vancouver Affordable Housing Endowment Fund) properties. Specifically, this work focuses on:

Identifying the count of properties in each neighborhood (Geo Local Area). Highlighting regions with more than 15 properties. Visualizing property concentration to support decision-making for resource allocation.

Dataset

1) Source: Dataset includes details on properties owned by VAHEF, such as: Building Number: Unique identifier for each property. Geo Local Area: Indicates the neighborhood where the property is located. Other attributes (omitted in this analysis for relevance).

2) Data Characteristics: Complete dataset with no missing values (as identified in the profiling step). Focus on Building Number and Geo Local Area for the analysis.

Methodology The analysis was conducted in four systematic steps: data ingestion, profiling, cleaning, and pipeline design.

image

Data Ingestion
Objective: Load raw data into AWS S3 for centralized storage and future processing.

Steps:

Created two S3 buckets:

Raw Data Bucket: For unprocessed data.

Transformed Data Bucket: For cleaned and structured data.

image

Data Profiling
Objective: Analyze the dataset to understand its structure and quality.

Steps:

Used AWS Glue DataBrew to perform a profiling job.

Verified the absence of missing or invalid data:

100% data availability for all columns.

Building Number uniquely identifies each property.

Focused on understanding the Geo Local Area column for grouping properties.

image

Data Cleaning
Objective: Remove irrelevant information and prepare the dataset for analysis.

Steps: Dropped unnecessary columns, focusing solely on Building Number and Geo Local Area.

Ensured no extra spaces, invalid characters, or outliers remained.

Transferred the cleaned dataset into a “Data Cleaning” folder within the transformed S3 bucket.

Created two output files:

Parquet Format: Stored in the system folder for efficient processing.

CSV Format: Stored in the user folder for accessibility.

image

Data Pipeline Design
Objective: Automate data processing and prepare outputs for visualization and insights.

Pipeline Workflow:

Source: Connected the cleaned dataset to the pipeline.

Transformation:

Grouped properties by Geo Local Area.

Counted the number of properties per area.

Applied a filter to identify neighborhoods with more than 15 properties.

Destination:

Saved the results in the transformed data bucket under a special folder for “Owned Properties.”

image

Exploratory Analysis

Objective: Provide deeper insights into the geographic distribution of VAHEF properties.

Steps:

Conducted a detailed analysis of the Geo Local Area column:

Extracted area names by removing numbers and special characters.

Focused on high-concentration areas like Downtown, Mount Pleasant, and Walter Harwick Street.

Created visualizations to highlight areas with high property concentrations.

Deliverable:

Identified key regions with significant property ownership.

image

Deliverables

Cleaned Dataset:

CSV and Parquet formats with columns: Building Number, Geo Local Area, and property counts.

image

ETL Pipeline: Configured for automated data processing and updating with new datasets. image

Visualization: Heatmaps or bar charts summarizing property distributions.

Analysis Report: Summary of findings, including high-concentration neighborhoods and insights for resource optimization.
