# Project-1

## Exploratory Data Analysis

### Project Description
**Project Title**  
DAP Design and Implementation (Individual Work - Venkata Sai Krishna Bhimavarapu)  

**Objective**  
The main aim of this project is to design and implement a Data Analytics Platform to determine:  
- How many cultural spaces exist in each local area.  
- The percentage of cultural spaces privately owned, government-owned, or operated by non-profits.  

The project utilizes an AWS S3 bucket to store the raw dataset, AWS Glue DataBrew for profiling and cleaning the data, and AWS Glue to build and manage the ETL pipeline.  

**Dataset**  
The dataset includes cultural spaces, their type, location, and ownership details.  

### Methodology
1. **Data Ingestion**  
   - Created two separate buckets:
     - `cul-spc-raw-ven`: For raw data.
     - `cul-spc-trf-ven`: For transformed data with folders like data profiling, data cleaning, and data quality.
   - Uploaded the raw dataset to the storage bucket.

   ![Figure 1: Storage Buckets](image-path-1)
   ![Figure 2: Raw Dataset](image-path-2)
   ![Figure 3: File Structure](image-path-3)

2. **Data Profiling**  
   - Used AWS DataBrew to connect the raw dataset and create a profiling job.
   - Analyzed the dataset for missing values, correlations, and data quality issues.

   ![Figure 4: AWS DataBrew Connection](image-path-4)
   ![Figure 5: Job Created](image-path-5)
   ![Figure 6: Correlation Analysis](image-path-6)
   ![Figure 7: Missing Values](image-path-7)
   ![Figure 8: Required Columns](image-path-8)

3. **Data Cleaning**  
   - Removed irrelevant columns while retaining useful ones.
   - Created structured cleaning projects and routed cleaned data to appropriate folders.

   ![Figure 9: Project Created](image-path-9)
   ![Figure 10: Cleaned Data](image-path-10)
   ![Figure 11: Recipe of Dataset](image-path-11)
   ![Figure 12: Recipe Details](image-path-12)
   ![Figure 13: Final Outputs](image-path-13)
   ![Figure 14: Output 1](image-path-14)
   ![Figure 15: Output 2](image-path-15)

4. **Data Pipeline Design**  
   - Built an AWS Glue ETL pipeline for transformations.
   - Removed unnecessary columns and grouped data by location to analyze ownership distribution.

   ![Figure 16: ETL Pipeline](image-path-16)
   ![Figure 17: Local Area Analysis](image-path-17)
   ![Figure 18: Ownership Distribution Pipeline](image-path-18)

### Tools and Technologies
- **AWS Services**: S3, Glue, DataBrew, Glue ETL
- **Programming Languages**: SQL
- **Other Tools**: AWS Console

### Deliverables
1. Ownership Distribution: Percentage of cultural spaces by ownership type (Private, Government, Non-Profit).  
   ![Figure 21: Ownership Distribution Output](image-path-21)  
2. Local Area Analysis: Concentration of cultural spaces in each local area.  
   ![Figure 20: Local Area Analysis Output](image-path-20)
3. Final ETL Pipeline: Ensuring efficient and repeatable processing for future datasets.  
   ![Figure 19: Descriptive ETL](image-path-19)
