# DAP Implementation (Individual Work) – Venkata Sai Krishna Bhimavarapu

## Step 5: Data Enriching
To prepare the data for analysis, I followed these steps:

1. **Created a DynamoDB Database**  
   - The database was scalable and flexible, capable of managing large volumes of data.
2. **Exported Data to S3**  
   - Exporting to S3 provided secure and cost-effective storage.
   - Enabled direct analytics using AWS tools like Glue and Athena.

![Figure 1: Exports to S3 from DynamoDB](https://raw.githubusercontent.com/username/repository/main/images/exports_to_s3.png)  
*Screenshot from AWS Console.*  

![Figure 2: Exported Objects Output](https://raw.githubusercontent.com/username/repository/main/images/exported_objects_output.png)  
*Screenshot from AWS Console.*  

3. **AWS Glue Crawler**  
   - Automatically inferred schema and populated the AWS Glue Data Catalog.
   - Ensured the data was query-ready for further analysis.


4. **Analyzed Data with AWS Athena**  
   - SQL queries were executed directly on the data stored in S3.
   - Ensured data integrity in terms of completeness, consistency, and uniqueness.

![Figure 4: SQL Query Execution in AWS Athena](https://raw.githubusercontent.com/username/repository/main/images/sql_query_execution.png)  
*Screenshot from AWS Console.*

---

## Step 6: Data Protection

### Encryption Techniques for Confidentiality
1. **AWS Key Management Service (KMS)**  
   - Created symmetric encryption keys for secure data encryption and decryption.
   - Integrated with other AWS services to ensure end-to-end encryption.

![Figure 5: Customer Managed Keys](https://raw.githubusercontent.com/username/repository/main/images/customer_managed_keys.png)  
*Screenshot from AWS Console.*

2. **Bucket-Level Encryption**  
   - Applied to ensure sensitive information is only accessible to authorized users.

![Figure 6: Bucket-Level Encryption](https://raw.githubusercontent.com/username/repository/main/images/bucket_level_encryption.png)  
*Screenshot from AWS Console.*

3. **Status of Buckets**  
   - Verified encryption status for all buckets.

![Figure 7: Bucket Status](https://raw.githubusercontent.com/username/repository/main/images/bucket_status.png)  
*Screenshot from AWS Console.*

### Integration by Means of Bucket Versioning
- **Purpose:** Maintain multiple versions of objects in S3 to enhance reliability and prevent accidental data loss.  
- **Benefits:**
  1. Data Recovery
  2. Audit Trail
  3. Protection Against Errors

![Figure 8: Enabling Bucket Versioning](https://raw.githubusercontent.com/username/repository/main/images/bucket_versioning.png)  
*Screenshot from AWS Console.*

---

## Step 7: Data Governance

1. **AWS Glue ETL Pipeline**  
   - Ensured data quality by safeguarding sensitive information and organizing processed data.

2. **Sensitive Data Detection**  
   - Verified that no Personally Identifiable Information (PII) was present.

![Figure 10: Detecting Sensitive Data](https://raw.githubusercontent.com/username/repository/main/images/sensitive_data_detection.png)  
*Screenshot from AWS Console.*

3. **Data Quality Evaluation**  
   - Assessed columns for completeness and identified areas with square footage greater than 10,000.

![Figure 11: Data Quality Pipeline](https://raw.githubusercontent.com/username/repository/main/images/data_quality_pipeline.png)  
*Screenshot from AWS Console.*

---

## Step 8: Data Observability

1. **Implemented AWS CloudWatch**  
   - Monitored data health, quality, and flow.  
   - Developed dashboards to track key metrics, detect anomalies, and manage costs.

![Figure 12: CloudWatch Dashboard](https://raw.githubusercontent.com/username/repository/main/images/cloudwatch_dashboard.png)  
*Screenshot from AWS Console.*

---

## Conclusion
This project successfully designed and implemented a robust Data Analytics Platform. The use of AWS services ensured efficient data storage, protection, governance, and observability, delivering high-quality insights and enabling decision-making.

**Note:** Replace the placeholders `https://raw.githubusercontent.com/username/repository/main/images/image_name.png` with the actual URLs of your uploaded images.
