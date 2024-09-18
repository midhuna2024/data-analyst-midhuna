# data-analyst-midhuna
# Data Analytic Platform for The City of Vancouver - Data Protection, Governance, and Monitoring

## Objective
The goal of this phase of the project was to ensure data protection, governance, and continuous monitoring for the animal lost and found data from the City of Vancouver using AWS services. This included encryption of data, maintaining data quality, implementing governance policies, and setting up monitoring to track key metrics and ensure security and performance.

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

## Data Governance

1. **Trusted Folders for Data Governance**:
   - Created separate folders in S3 (named `Trusted`) to store high-quality data that passed governance checks and filtering rules. 
   - Set up workflows to automate the governance process.
     - Workflow Name: `project-anilost24-dqdp-midhuna`
     - Automated scheduling was implemented to run governance checks every Sunday at 11:59 PM.

2. **Data Quality and Privacy Evaluation**:
   - Built data pipelines using AWS Glue to filter and validate the data, ensuring it met governance policies.
   - Data that passed the checks was stored in the trusted folder for further analysis.

## Data Monitoring

1. **CloudWatch for Monitoring**:
   - Set up CloudWatch dashboards to monitor various metrics, including billing and storage usage for the project.
     - Dashboard Name: `project-anilost-dashboard-midhuna`
     - Two widgets were created: one for estimated billing charges and one for storage service usage.
     - Set up an alarm to notify if costs exceed $38 for S3 usage.
       - Alarm Name: `project-anilost2024-alarm-midhuna`
   - CloudTrail was used to monitor API calls and track access to resources, ensuring secure and accountable use of the AWS environment.
     - Trail Name: `project-anilost-trail-midhuna`

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










