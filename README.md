# data-analyst-midhuna
# Data Analytic Platform for City of Vancouver - Animal Lost Data Analysis

## Objective
The primary objective of this project was to analyze the lost and found dog data from the City of Vancouver for 2023 and 2024. The aim was to determine the percentage of lost dogs relative to the total number of dogs in the dataset. The analysis provides insights into the trends in dog loss over the two years, helping city officials with resource allocation and response strategies.

## Dataset
The dataset used in this project was sourced from the City of Vancouver's open data portal. It contains detailed information about lost and found dogs for the years 2023 and 2024. Key fields in the dataset include:
- Dog ID
- Status (Lost or Found)
- Date of the record
- Other relevant attributes

## Methodology
<img width="598" alt="1" src="https://github.com/user-attachments/assets/832b2b61-3627-4a96-b503-4ba9bb412227">


1. **Data Discovery**:  
   Extracted relevant data from the City of Vancouver’s open data portal, focusing on lost and found dog records for 2023 and 2024.
   ![image](https://github.com/user-attachments/assets/1bd01eb7-a08d-466f-8aca-e5adea0b7fb6)


2. **Data Storage Design**:  
   Created separate S3 buckets for storing raw, cleaned, and curated data for 2023 and 2024. Data was ingested into S3 using AWS services.
   ![image](https://github.com/user-attachments/assets/6750d677-8454-4c9e-9de0-5469bd2ef0d7)


3. **Dataset Preparation**:  
   Cleaned and reduced the dataset to 200 records for both years to optimize cost and processing speed.
   ![image](https://github.com/user-attachments/assets/80afa5dd-3537-4dc3-90ef-a795cdf658cd)


4. **Data Ingestion**:  
   Uploaded the dataset into the S3 landing folder for both years and used Glue DataBrew to structure the data.
   ![image](https://github.com/user-attachments/assets/22181427-e911-4ab8-8d57-8b45c4602f69)
   

5. **Data Cleaning**:
   - **Removing Unnecessary Columns**: Removed columns that were not relevant to the analysis, such as irrelevant identifiers or attributes.
   - **Handling Missing Values**: Missing values were identified and appropriately dealt with either by:
     - Removing records that had insufficient information.
     - Imputing missing values if necessary.
   - **Formatting Data**: Ensured that all fields (such as dates and categorical variables) were formatted correctly for analysis, such as converting text fields into appropriate formats.
     ![image](https://github.com/user-attachments/assets/3d577260-1558-4cb5-8561-d3a436a687f2)


6. **Data Structuring**:
   - **Schema Changes**: The dataset schema was restructured to make the data easier to work with:
     - Renamed columns for better readability (e.g., “DogStatus” instead of ambiguous names).
     - Created new columns by extracting data (e.g., extracting the "Year" from a date column).
       ![image](https://github.com/user-attachments/assets/665dfde0-470e-4d1c-a5a3-3e28fa93f8d8)

   
7. **Data Pipeline Design and Implementation**:  
   Designed an ETL (Extract, Transform, Load) pipeline using AWS Glue DataBrew to clean and transform the data. The pipeline involved removing unnecessary columns and calculating the percentage of lost dogs using the formula:
   
![image](https://github.com/user-attachments/assets/4630adc8-3fdd-4e15-856a-6f7e9eb9294d)
![image](https://github.com/user-attachments/assets/9f39e9de-e31e-4986-99b3-92c715c7a450)
![image](https://github.com/user-attachments/assets/34c77b77-7c31-4440-b9df-ed162eda6606)

Percentage of Dogs Lost = (Total Number of Dogs / Number of Lost Dogs) × 100
8. **Data Analysis**:
7. ![image](https://github.com/user-attachments/assets/3b2e43b6-7764-4f80-9aba-bf895ec1b198)

Queried the cleaned and structured data using Amazon Athena to calculate the percentage of lost dogs for 2023 and 2024.

9. **Data Visualization**:
=. ![image](https://github.com/user-attachments/assets/d901e7be-19d6-4b1b-ab01-3a410e9147b4)

Used Amazon QuickSight to visualize trends in the data, including the percentage of lost dogs across the two years.

10. **Data Publishing**:  
Results were published via an EC2 server for internal access.
![image](https://github.com/user-attachments/assets/a332999c-2013-40b8-a642-36293e0a726c)
![image](https://github.com/user-attachments/assets/f544a338-9c60-4eda-bf32-9289d41f2081)
![image](https://github.com/user-attachments/assets/0fe93356-e387-4576-be3a-d39239d688f1)


## Tools and Technologies

- **AWS S3**: For data storage at various stages (raw, cleaned, and curated).
- **AWS Glue & Glue DataBrew**: For data cleaning, structuring, and building the data pipeline.
- **Amazon Athena**: For querying the data and performing analyses.
- **Amazon QuickSight**: For data visualization.
- **AWS EC2**: For hosting the published results and making them accessible to stakeholders.
- **AWS Glue DataBrew**: Used to automate the data cleaning and structuring process, allowing for step-by-step transformations.
- **AWS S3**: Data was stored at various stages (raw, cleaned, and structured) to maintain different versions of the dataset.
- **Amazon Athena**: For running queries to ensure that the cleaning and structuring were successful and that the data was in the correct format for further analysis.


## Deliverables

- A curated dataset stored in AWS S3, representing the clean and structured lost and found dog data for 2023 and 2024.
- Analytical results, including the percentage of lost dogs, published via EC2.
- Visualized trends of lost dogs using Amazon QuickSight.
- A cleaned version of the dataset with missing or incorrect values removed or corrected.
-  A well-structured dataset, stored in AWS S3, partitioned by year, and ready for analysis with Amazon Athena.
-  Automated jobs to repeat the data cleaning and structuring process as needed.

  This project highlights the ability to perform end-to-end data analysis using AWS cloud services, including data ingestion, cleaning, transformation, analysis, and visualization, to provide actionable insights to the City of Vancouver.

