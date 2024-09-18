# data-analyst-midhuna
# UCW Research Ethics 

## Overview
The goal of this project is to build a secure, governed, and monitored data platform for managing research ethics data for UCW. The platform focuses on protecting sensitive research application data, maintaining data quality, and providing continuous monitoring for performance and security. it involves building a secure, governed, and monitored platform for UCW's Research Ethics data, using AWS services like S3, KMS, CloudWatch, Glue, and Athena. The data contains research application submissions from 2023 and 2024.
## Methodology
![3](https://github.com/user-attachments/assets/87e4be47-971e-4d4f-a49f-fb6e59a82cce)


## Steps
1. **Data Discovery**: Extraction of research ethics data.
   <img width="960" alt="aws console" src="https://github.com/user-attachments/assets/7ce668e6-dde8-480b-aa11-264aaef2c3ce">

3. **Data Storage Design**: Setup of S3 buckets for raw, cleaned, and curated data.
4. **Dataset Preparation**: Data cleaning and structuring.
   <img width="960" alt="aws3" src="https://github.com/user-attachments/assets/03c026c4-771b-405b-a429-19a14d97b860">
   <img width="960" alt="cp#4" src="https://github.com/user-attachments/assets/f5c76d59-7c54-4c8d-b2c8-0f10befe3513">


6. **Data Pipeline**: Building ETL processes using AWS Glue.
   <img width="960" alt="etl" src="https://github.com/user-attachments/assets/d1ace023-3cda-4a91-a23a-24822d03de87">
   <img width="960" alt="aws ETL" src="https://github.com/user-attachments/assets/ba3c01b1-ef49-4a99-b543-450c6172a3ca">


8. **Data Protection**: Applying KMS and encryption to protect data.
   <img width="960" alt="kms" src="https://github.com/user-attachments/assets/7f64908c-9213-481d-8368-2f07ff7ae794">
  

9. **Data Governance**: Implementing automated governance rules.
    <img width="960" alt="etl" src="https://github.com/user-attachments/assets/0ff6f559-dc9c-4c6c-86b5-7a072c719ea3">

     <img width="960" alt="wf" src="https://github.com/user-attachments/assets/1f50e271-1254-4b94-a999-92b353db4cb0">

11. **Data Monitoring**: Setup CloudWatch and CloudTrail for continuous monitoring.
    <img width="957" alt="2" src="https://github.com/user-attachments/assets/855b925a-1a6c-4bc8-a1a6-2527cdea933c">
    <img width="960" alt="3" src="https://github.com/user-attachments/assets/8e70a7e4-e27f-4797-bf02-bbe7ba4cf08d">


13. **Data Analysis**: Using Amazon Athena to analyze data.
14. **Data Visualization**: Visualization via Amazon QuickSight.

## Technologies
- AWS S3
- AWS KMS
- AWS Glue & Glue DataBrew
- Amazon Athena
- Amazon QuickSight
- AWS CloudWatch & CloudTrail


 
