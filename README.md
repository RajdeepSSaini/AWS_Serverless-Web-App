# Deploying a Serverless Web Application with AWS Lambda, API Gateway, and DynamoDB

## Overview
This project demonstrates how to deploy a serverless web application using AWS Lambda, API Gateway, and DynamoDB. The tutorial covers the creation of an IAM role, a Lambda function, a DynamoDB table, and the configuration of API Gateway to handle requests.

## Prerequisites
Before you start, ensure you have the following:
- An AWS account
- Basic knowledge of AWS services (Lambda, DynamoDB, API Gateway)
- AWS CLI configured on your local machine

## Project Components
1. **DynamoDB**: Acts as the backend database storage.
2. **Lambda**: Functions as the web server.
3. **API Gateway**: Serves as the frontend interface.

## Project Setup

### Step 1: Create an IAM Role for Lambda
1. Navigate to the IAM console.
2. Click on **Roles** and then **Create role**.
3. Select **Lambda** under the service options.
4. Attach the following policies:
    - `AWSLambdaBasicExecutionRole`
    - `AmazonDynamoDBFullAccess`
5. Name the role (e.g., `lambda-dynamo-role`) and create it.

### Step 2: Create a DynamoDB Table
1. Navigate to the DynamoDB console.
2. Click on **Tables** and then **Create table**.
3. Set the table name to `AAS_table` and the partition key to `email` (String).
4. Leave the default settings and create the table.

### Step 3: Create a Lambda Function
1. Navigate to the Lambda console.
2. Click on **Create function**.
3. Set the function name (e.g., `aas-demo-function`), choose Python 3.8 as the runtime.
4. Under **Execution role**, select **Use an existing role** and choose the role created in Step 1.
5. Create the function.

### Step 4: Upload the Lambda Function Code
1. Prepare a ZIP file containing the following files:
    - `lambda_function.py`
    - `contact_us.html`
    - `success.html`
2. In the Lambda console, upload the ZIP file to the function.
3. Ensure the Lambda function code handles GET and POST requests to serve the HTML pages and interact with DynamoDB.

### Step 5: Configure API Gateway
1. Navigate to the API Gateway console.
2. Click on **Create API** and choose **REST API**.
3. Name the API (e.g., `demo-api`) and create it.
4. Create methods for GET and POST requests:
    - For GET, integrate with the Lambda function.
    - For POST, integrate with the Lambda function.
5. Deploy the API and note the invoke URL.

## Usage
1. Access the invoke URL from the API Gateway in your browser.
2. Fill out the contact form and submit it.
3. Check DynamoDB to see the stored entries.

## Files
- **lambda_function.py**: Contains the Lambda function code.
- **contact_us.html**: The contact form served by the Lambda function.
- **success.html**: The success page is displayed upon successful form submission.

## Conclusion
This project demonstrates the integration of AWS Lambda, DynamoDB, and API Gateway to create a serverless web application. By following the steps, you can deploy and test the application on AWS.

## License
This project is licensed under the MIT License.

## Contact
If you have any questions, feel free to reach out:

- **Name:** Rajdeep Singh Saini
- **Email:** [singhsainirajdeep@example.com](mailto:singhsainirajdeep@example.com)
- **GitHub:** [Rajdeep Singh Saini](https://github.com/RajdeepSSaini)

