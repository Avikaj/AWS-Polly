# AWS-Polly

## Introduction

Convert any uploaded **.txt** file in an S3 bucket into an **MP3** using **Amazon Polly**, via an **AWS Lambda** function triggered by S3 events.

## Prerequisites

* AWS account + AWS CLI configured
* **AWS SAM CLI**
* Python 3.11

## Uses
1. Accessibility (WCAG/ADA): Provide audio alternatives for policies, help pages, handbooks, study guides—created automatically on upload.

2. E-learning narration: Convert lesson scripts to MP3 for LMS modules; versioned in S3, swapped per course update.
3. Audio newsletters & podcasts: Convert long-form posts into episodic MP3s; stitch segments and publish a feed.

4. Multilingual announcements: Generate localized audio by switching Polly voices/languages for product updates or kiosk announcements.

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



