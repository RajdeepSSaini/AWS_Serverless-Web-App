# Serverless Web Application on AWS
Welcome to the repository for my serverless web application project on AWS! This project leverages various AWS services to create a fully functional serverless web application. Below, you'll find an overview of the project's architecture and the steps involved in setting up the application.

## Project Overview
This project demonstrates how to deploy a serverless web application on AWS. The application uses an S3 bucket to host static web content, API Gateway to handle API requests, Lambda functions for backend processing, DynamoDB for data storage, and CloudFront for secure and efficient content delivery.

## 1. Setting up an S3 Bucket
The S3 bucket is used to host the static web content, including HTML, CSS, and JavaScript files.

## 2. Configuring API Gateway
API Gateway endpoints are configured to trigger Lambda functions. Both GET and POST methods are set up to interact with the DynamoDB database.

## 3. Creating Lambda Functions
Lambda functions written in Python handle the API Gateway requests. These functions include retrieving data from DynamoDB and inserting new data into it.

## 4. Working with DynamoDB
A DynamoDB table is set up to store the application's data. The table schema is defined, and CRUD operations are performed using Lambda functions.

## 5. Implementing Secure Connections with CloudFront
CloudFront is deployed as a content delivery network (CDN) to ensure secure access to the web application. It serves the S3 content securely over HTTPS, providing encryption in transit and improving the application's performance.

## Conclusion
This project showcases a serverless architecture on AWS, capable of securely handling user requests, storing data in DynamoDB, and delivering content efficiently using CloudFront. It serves as a practical example of how to build and deploy a serverless web application.

## License
This project is licensed under the MIT License.

## Contact
If you have any questions, feel free to reach out:

- **Name:** Rajdeep Singh Saini
- **Email:** [singhsainirajdeep@example.com](mailto:singhsainirajdeep@example.com)
- **GitHub:** [Rajdeep Singh Saini](https://github.com/RajdeepSSaini)

Happy Coding!
