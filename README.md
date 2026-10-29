# AWS S3 Event-Driven Automation Using Lambda

## 📌 Project Overview

This project demonstrates event-driven automation using Amazon S3 and AWS Lambda. Whenever a CSV file is uploaded to an S3 bucket, an S3 event automatically triggers a Lambda function. The function processes the event, extracts the bucket name and uploaded file name, and logs the details in Amazon CloudWatch.

## 🏗️ Architecture

```text
User Uploads CSV File
         |
         v
   Amazon S3 Bucket
         |
         v
   S3 Event Notification
      (Object Created)
         |
         v
     AWS Lambda
     (Python Code)
         |
         v
   Amazon CloudWatch
      (Execution Logs)
```

## 🛠️ AWS Services Used

- **Amazon S3:** Stores the customer CSV file.
- **AWS Lambda:** Executes Python code automatically when triggered by an S3 event.
- **Amazon CloudWatch:** Stores Lambda execution logs for monitoring and debugging.
- **AWS IAM:** Provides permissions for Lambda to write logs.

## 📂 Input Dataset

The project uses a file named `customers.csv`.

Example dataset:

| customer_id | name | email | city | status |
|---|---|---|---|---|
| 101 | Tharun | tharun@example.com | Bengaluru | Active |
| 102 | Rahul | rahul@example.com | Hyderabad | Active |
| 103 | Priya | priya@example.com | Chennai | Inactive |
| 104 | Arun | arun@example.com | Mumbai | Active |
| 105 | Meena | meena@example.com | Pune | Inactive |

## ⚙️ Implementation Steps

1. Created an Amazon S3 bucket.
2. Uploaded the `customers.csv` file to the bucket.
3. Created an AWS Lambda function using Python.
4. Added Python code to capture S3 event details.
5. Configured an S3 trigger for CSV uploads.
6. Uploaded the CSV file again to generate a new event.
7. Checked the execution results in Amazon CloudWatch Logs.

## 💻 Lambda Functionality

The Lambda function:

- Receives S3 event notifications.
- Extracts the bucket name.
- Retrieves the uploaded file name.
- Checks whether the uploaded file has a `.csv` extension.
- Prints the processing status to CloudWatch Logs.

## ✅ Expected Output

```text
S3 Event Triggered Successfully!
Bucket Name: your-s3-bucket-name
Uploaded File: customers.csv
CSV file detected successfully!
```

*Note: The bucket name in the output depends on your actual S3 bucket.*

## 🔐 Security and Permissions

- Kept S3 Block Public Access enabled.
- Used an IAM execution role for Lambda.
- Enabled CloudWatch logging through basic Lambda execution permissions.
- Configured an S3 event notification to invoke the Lambda function.

## 🎯 Learning Outcomes

- Understanding event-driven architecture in AWS.
- Configuring S3 event notifications.
- Creating and deploying Python-based Lambda functions.
- Integrating AWS services through event triggers.
- Monitoring serverless applications using CloudWatch Logs.
- Understanding basic IAM permissions.

## 🚀 Future Enhancements

- Read and validate CSV file contents.
- Store processed data in a separate S3 bucket or folder.
- Send email notifications after successful processing.
- Add error handling and failure notifications.
- Build a complete serverless data processing pipeline.

## 👨‍💻 Author

**Kannaiahgari Tharun**

GitHub: [Kannaiahgaritharun](https://github.com/Kannaiahgaritharun)


