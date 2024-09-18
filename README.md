# data-analyst-midhuna
# UCW Research Ethics 

## Overview
The goal of this project is to build a secure, governed, and monitored data platform for managing research ethics data for UCW. The platform focuses on protecting sensitive research application data, maintaining data quality, and providing continuous monitoring for performance and security. it involves building a secure, governed, and monitored platform for UCW's Research Ethics data, using AWS services like S3, KMS, CloudWatch, Glue, and Athena. The data contains research application submissions from 2023 and 2024.
## Methodology
![3](https://github.com/user-attachments/assets/87e4be47-971e-4d4f-a49f-fb6e59a82cce)


## Steps
1. **Data Discovery**: Extraction of research ethics data.
   
   <img width="960" alt="Screenshot 2024-09-17 225227" src="https://github.com/user-attachments/assets/20eb6f70-623f-4bb6-ae58-4389912ce3ef">


2. **Data Storage Design**: Setup of S3 buckets for raw, cleaned, and curated data.
   <img width="960" alt="aws console" src="https://github.com/user-attachments/assets/7ce668e6-dde8-480b-aa11-264aaef2c3ce">
   <img width="947" alt="raw" src="https://github.com/user-attachments/assets/042e793a-d1f4-4ca9-b697-218069534341">
   <img width="932" alt="curated" src="https://github.com/user-attachments/assets/4c8f574d-ec0e-403b-8589-cc987f477414">
   <img width="956" alt="trusted" src="https://github.com/user-attachments/assets/7215da59-f965-481e-9770-f6e81916dc15">



   
3. **Dataset Preparation**: Data cleaning and structuring.
   <img width="960" alt="aws3" src="https://github.com/user-attachments/assets/03c026c4-771b-405b-a429-19a14d97b860">
   

4. **Data Pipeline**: Building ETL processes using AWS Glue.
   
   <img width="960" alt="aws ETL" src="https://github.com/user-attachments/assets/ba3c01b1-ef49-4a99-b543-450c6172a3ca">


5. **Data Protection**: Applying KMS and encryption to protect data.
   <img width="960" alt="kms" src="https://github.com/user-attachments/assets/7f64908c-9213-481d-8368-2f07ff7ae794">
  

6. **Data Governance**: Implementing automated governance rules.
    <img width="960" alt="etl" src="https://github.com/user-attachments/assets/0ff6f559-dc9c-4c6c-86b5-7a072c719ea3">

     <img width="960" alt="wf" src="https://github.com/user-attachments/assets/1f50e271-1254-4b94-a999-92b353db4cb0">

7. **Data Monitoring**: Setup CloudWatch and CloudTrail for continuous monitoring.
    <img width="957" alt="2" src="https://github.com/user-attachments/assets/855b925a-1a6c-4bc8-a1a6-2527cdea933c">
    <img width="960" alt="3" src="https://github.com/user-attachments/assets/8e70a7e4-e27f-4797-bf02-bbe7ba4cf08d">


8. **Data Analysis**: Using Amazon Athena to analyze data.
    <img width="960" alt="cp#4" src="https://github.com/user-attachments/assets/f5c76d59-7c54-4c8d-b2c8-0f10befe3513">

9. **Data Visualization**: Visualization via Amazon QuickSight.
    <img width="748" alt="graph" src="https://github.com/user-attachments/assets/c07605de-49b0-4274-b6ef-9b223480e14d">

    
10. **Data publishing**:Through general and web servers.
    <img width="960" alt="data vis step12" src="https://github.com/user-attachments/assets/28026c6e-a1b4-4406-ace2-c0df4226c87b">
    <img width="960" alt="web" src="https://github.com/user-attachments/assets/adfdcbb7-be9c-4dea-baa8-bf3b9b052c31">
    <img width="1031" alt="ws step 13" src="https://github.com/user-attachments/assets/947a61f6-f6ae-472a-82ca-3ef91b933589">



    

## Technologies
- AWS S3
- AWS KMS
- AWS Glue & Glue DataBrew
- Amazon Athena
- Amazon QuickSight
- Aws vpc
- Aws ec2
- AWS CloudWatch & CloudTrail
  The project not only achieves its objective of creating a secure, governed, and monitored data platform but also lays the groundwork for future scalability and integration with other datasets or research domains. This platform can be expanded to incorporate additional features such as machine learning models, more advanced data visualizations, and predictive analytics, all of which will further enhance UCW's research capabilities.

By following these steps, the platform demonstrates its value as a reliable, secure, and insightful tool for managing research ethics data at UCW, ensuring the highest levels of data  storage , retrieving, accessing, security, governance, and usability.


 
