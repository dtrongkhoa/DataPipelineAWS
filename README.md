# DataPipelineAWS

A data pipeline using AWS services, orchestrated by Airflow

# Details

1. Extract - Get the data through https://openweathermap.org/
2. Transform - Execute data transformation using python from JSON file
3. Load - Load data into S3 Bucket with CSV format
4. Orchestrate - Use Airflow to orchestrate the process

# How to run the project

1. Launch an EC2 instance:
   a. Set inbound rules: Custom TCP, Port range: 8080, Source: anywhere
   b. Install Python, Pip
   c. Create a virtual environment
   d. Inside the virtual environment, install Pandas, Apache Airflow, s3fs and awscli
2. Create a role with S3FullAccess and EC2FullAccess
3. Create a user
4. Inside airflow folder in ec2, create DAGS folder then add this python file inside that DAGs folder
5. Retrieve access id, secret id and token through awscli
6. Create a seperate python file to store those credentials
7. Create an account on https://openweathermap.org/ and get the API
8. Update API key and s3 bucket name inside python file
