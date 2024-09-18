# data-analyst-midhuna
# Data Analytic Platform for The City of Vancouver - Data Protection, Governance, and Monitoring

## Objective
The goal of this phase of the project was to ensure data protection, governance, and continuous monitoring for the animal lost and found data from the City of Vancouver using AWS services. This included encryption of data, maintaining data quality, implementing governance policies, and setting up monitoring to track key metrics and ensure security and performance.
<img width="932" alt="2" src="https://github.com/user-attachments/assets/492d022c-9e9f-4304-a941-613b48755a05">


## Data Protection

1. **KMS (Key Management Service)**:  
   - Created a KMS key for encrypting the data stored in S3 buckets, ensuring that only authorized users can access the protected data.
     - Key Name: `project-animallost-key-midhuna`
   - Assigned the key to the S3 bucket for automatic encryption at rest, ensuring that all data uploaded to the bucket is encrypted to meet security best practices.
   - **Backup Strategy**:
     - Created a backup S3 bucket: `project-animallost-backup-midhuna`
     - Set up replication rules and enabled versioning to ensure that backup copies of data were created and previous versions were stored, preventing accidental overwriting or deletion.
      

2. **Data Encryption**:
   - Each team member set up KMS keys for their respective projects to protect sensitive datasets.
   - The encryption applied ensures compliance with data protection standards.
     <img width="935" alt="1" src="https://github.com/user-attachments/assets/e8b2e38b-066c-4332-88eb-396184766a0f">
     <img width="946" alt="2" src="https://github.com/user-attachments/assets/aa4a65da-a550-412b-883c-fb4c5fd1c98e">
     <img width="939" alt="3" src="https://github.com/user-attachments/assets/4f0a4622-5fd1-41ff-bfa6-756c82f4d169">
     <img width="950" alt="4" src="https://github.com/user-attachments/assets/790994a0-3d88-4d3f-876d-ee894d7058b3">


## Data Governance

1. **Trusted Folders for Data Governance**:
   - Created separate folders in S3 (named `Trusted`) to store high-quality data that passed governance checks and filtering rules. 
   - Set up workflows to automate the governance process.
     - Workflow Name: `project-anilost24-dqdp-midhuna`
     - Automated scheduling was implemented to run governance checks every Sunday at 11:59 PM.

2. **Data Quality and Privacy Evaluation**:
   - Built data pipelines using AWS Glue to filter and validate the data, ensuring it met governance policies.
   - Data that passed the checks was stored in the trusted folder for further analysis.
   <img width="960" alt="1" src="https://github.com/user-attachments/assets/8a29b7f9-1ad6-4d2e-b3a4-fe01edb6f558">
   <img width="960" alt="2" src="https://github.com/user-attachments/assets/011c4b2a-b244-49e9-8417-b28391d67891">
   <img width="960" alt="3" src="https://github.com/user-attachments/assets/3e66f16b-e822-468e-b802-083b79343ebd">
   <img width="960" alt="4" src="https://github.com/user-attachments/assets/f43d9198-eb6d-4611-8ba1-9d87f1a220ae">
   <img width="960" alt="5" src="https://github.com/user-attachments/assets/67a0690e-f7ce-40ee-9841-8533ba214a3b">

  
## Data Monitoring

1. **CloudWatch for Monitoring**:
   - Set up CloudWatch dashboards to monitor various metrics, including billing and storage usage for the project.
     - Dashboard Name: `project-anilost-dashboard-midhuna`
     - Two widgets were created: one for estimated billing charges and one for storage service usage.
     - Set up an alarm to notify if costs exceed $38 for S3 usage.
       - Alarm Name: `project-anilost2024-alarm-midhuna`
   - CloudTrail was used to monitor API calls and track access to resources, ensuring secure and accountable use of the AWS environment.
     - Trail Name: `project-anilost-trail-midhuna`
       <img width="958" alt="1" src="https://github.com/user-attachments/assets/43e7edab-4866-4380-9cbe-b527e474d098">
       <img width="960" alt="2" src="https://github.com/user-attachments/assets/cce3107e-9489-4490-be56-aa7b6c879175">
       <img width="958" alt="3" src="https://github.com/user-attachments/assets/6a092a33-c24c-43b0-aff2-ea24846c5f62">
       <img width="960" alt="4" src="https://github.com/user-attachments/assets/13f188fe-5841-4c8c-a566-82cdc8925f46">
       <img width="960" alt="5" src="https://github.com/user-attachments/assets/96cccdb9-3d63-49e0-8367-11e313734b88">

## Tools and Technologies

- **AWS S3**: Used for data storage at various stages (Landing, Raw, Trusted).
- **AWS KMS**: To ensure data encryption and protect sensitive data.
- **AWS Glue**: For building ETL pipelines and automating data governance.
- **AWS CloudWatch**: For monitoring costs, performance, and resource usage.
- **AWS CloudTrail**: To audit and monitor API access and ensure security.

## Deliverables

- **Encrypted Datasets**: S3 buckets encrypted with KMS, ensuring data is secure.
- **Data Governance Pipelines**: Workflows to ensure that only high-quality data is stored in the trusted folders.
- **CloudWatch Dashboards**: For real-time monitoring of the project's health and cost efficiency.
- **CloudTrail Logs**: To provide a detailed audit trail of API activity in the environment.

  conclusion highlights the successful integration of AWS services and the security, governance, and monitoring achievements of the project, reinforcing the importance of these features for the platform's overall efficiency and reliability.










