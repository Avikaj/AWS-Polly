# AWS-Polly

## Introduction

## Uses

## Project Layout


## Steps

### Step 1: Create two S3 Buckets

Bucket 1: aws-polly-source-bucket
Bucket 2: aws-polly-dest-bucket

### Step 2: Createa an IAM Policy
IAM Policy name: convertor-polly-policy

<img width="1512" alt="Screenshot 2025-02-01 at 6 45 00 PM" src="https://github.com/user-attachments/assets/92f8830f-633e-45d9-b63c-cc230f0f0747" />

### Step 3: Create an IAM Role for the Policy

IAM Role: PollyRole and attach amc-polly-lambda-policy and AWSLambdaBasicExecutionRole Policies
<img width="1479" alt="Screenshot 2025-02-01 at 6 49 24 PM" src="https://github.com/user-attachments/assets/08ce716c-5cf7-4fd5-be73-c7afc385ba5d" />


### Step 4: Create the Lambda Funtion

Function Name: Text-to-Speech-proj
Use the Role created above, and add both buckets as environmental variables
<img width="1512" alt="Screenshot 2025-02-01 at 6 52 18 PM" src="https://github.com/user-attachments/assets/f8680a50-496c-4bfd-a6d1-2955d1143a84" />


### Step 5: Add a Trigger to the Lambda Function
<img width="1094" alt="Screenshot 2025-02-01 at 6 53 52 PM" src="https://github.com/user-attachments/assets/6d6637c7-7382-4afc-bc9c-de2bde345bab" />

### Step 6: Add the Lambda Code function
Paste the python code given to the Lambda function.

### Step 7: Test the System



