# Data Engineering using AWS

This project demonstrates an end-to-end data engineering pipeline using various AWS services. The architecture comprises an application part, an ETL part, and a transformation layer, ensuring a seamless data flow from data ingestion to data transformation and storage.

### Project Architecture

![Architecture](https://github.com/user-attachments/assets/b28f4d2c-2133-4b66-a967-93647e52af7b)
.

### Components

1. **Application Part:**
   - **EC2 Instance:** A Python Flask API is deployed on an EC2 instance to serve as the frontend and application logic layer.
   - **DynamoDB:** Data from the Flask API is stored in DynamoDB.

2. **ETL Part:**
   - **Lambda Function:** AWS Lambda functions are used to extract data from DynamoDB and load it into an S3 bucket (Staging Layer).
   - **S3 Bucket (Staging Layer):** Acts as the staging area for data before processing.
   - **AWS Glue:** Used for data cataloging, transforming, and preparing the data for analysis.
   - **CloudWatch:** Monitors the ETL processes and provides logging and alerting.

3. **Transformation Layer:**
   - **AWS Athena:** Used to query and analyze the data stored in the S3 bucket.
   - **Warehouse S3 Bucket:** Final transformed data is stored here for further use.

## Project Setup

### Prerequisites

- AWS account with necessary permissions
- Python 3.x
- Flask
- AWS CLI configured with your credentials

### Steps

1. Set up the Virtual Environment:

   ```
      python3 -m  myvenv
      cd venv\Scripts\activate --- On Windows
   ```

2. Install Dependencies:

   ```
      pip install flask
      pip install gunicorn
   ```

3. Run the Flask API Locally:

   ```
      python run.py

   ```

4. Deploy the Flask API to an EC2 Instance


5. Set Up Nginx Webserver


6. Create Lambda Layer

   ```
      mkdir lambda_layer
      cd lambda_layer
      pip install pandas -t .
      pip install boto3 -t .
      zip -r lambda_layer.zip .

   ```
