
***Project Scarecrow - README***
###
***Introduction***

Project Scarecrow is a SaaS platform for farmers to identify and deter farm pests using natural, humane methods. It leverages AWS services to provide real-time pest detection through machine learning and automated deterrents like sound, water, and light. The platform includes a dashboard for visualizing pest data, powered by Amazon QuickSight, with a secure and scalable architecture built on AWS.
***
###
***Problem Statement***
Farmers need an efficient and cost-effective solution to naturally scare pests away from their farms while ensuring security and global availability.

***Scope***
* Design: Build a globally available, secure, and compliant web app.
* Documentation: Ensure clear documentation of all project stages.
* Implementation: Use AWS services to create a SaaS solution that identifies and scares pests.
* Presentation: Deliver a scalable and user-friendly platform with real-time analytics.
***

###
***Key Features***
* Real-time Pest Detection: Machine learning model to identify pests.
* Automated Pest Deterrents: Trigger actions like sound, light, and water.
* Compliance: GDPR and PCI DSS compliance using AWS WAF, Cognito, KMS, and more.
* High Availability & Scalability: Use AWS Amplify, CloudFront, and Lambda for a globally distributed, scalable solution.
* Real-Time Dashboards: Customer-specific dashboards via Amazon QuickSight.

###
***Requirements***
* Cost-effective: Serverless architecture using AWS Lambda and Amazon S3.
* Compliance: AWS tools for security and audit (e.g., CloudTrail, Artifact).
* High Availability: Global content delivery with Amazon CloudFront.
* Distributed Workforce: Version control with AWS CodeCommit.

***
###
***Solution Overview***
The project uses the following AWS services:

* SageMaker: For pest detection model training.
* IoT Greengrass: To capture farm data.
* DynamoDB: Real-time data storage.
* QuickSight: Visualizes pest data.
* Amplify & CloudFront: Frontend hosting and global delivery.
* Cognito & WAF: Security and user authentication.
* CloudWatch & CloudTrail: For monitoring and logging.
***
###

***Architecture Summary***
* IoT Devices: Capture farm data (images, videos) using IoT cameras.
* Amazon S3: Stores raw data, which is used for training.
* SageMaker: Trains a machine learning model to detect pests.
* Lambda Functions: Triggers smart devices and forwards data.
* DynamoDB & Athena: Stores and queries real-time pest data.
* QuickSight: Displays dashboards for pest activity.
* Amplify: Hosts the frontend web application.
* CloudFront: Provides global content distribution.
* Cognito & WAF: Manage user authentication and secure the app.



***Requirements Breakdown***
Req ID	Requirement	Status	Comments
1.	CodeCommit repository:	Repository scarecrow_repo created with CFN stack
2.	Branches to the repository:	Webapp, architecture, IaC, and ML branches set
3.	Training of model using Amazon SageMaker: SageMaker used for model training
4.	Simulation of real-time farm data (IoT Greengrass): Lambda function triggered by CloudWatch event
5.	Web application	:Hosted on AWS Amplify
6.	Quicksight session: Customer-specific dashboards available
7.	Monitoring and Compliance: AWS Config and CloudWatch ensuring compliance

***

***Alternatives Considered***

* Option 1: SageMaker + S3 + Lambda on IoT Greengrass + Kinesis data streams + Quicksight + WAF + Cognito
* Option 2: SageMaker + DynamoDB + S3 + Athena + Quicksight + Amplify + Route 53 + WAF
***

***Selected Option:*** SageMaker + DynamoDB + Athena + Quicksight + Lambda + Amplify + Route 53 + WAF

***

***Major Decisions***
* AWS Amplify vs. EC2: Amplify was chosen for its serverless capabilities, ease of integration, scalability, and cost-efficiency.
* DynamoDB vs. S3 for Database: DynamoDB was chosen for real-time data handling without requiring cataloging (unlike S3).

***Diagrams***
* Main Architecture: Shows the flow of IoT data, S3 storage, machine learning process, and real-time visualization.
* SageMaker Process: Depicts the machine learning model training.
* IoT Simulation: Shows how IoT devices collect farm data.
* CI/CD Pipeline: Illustrates the integration of infrastructure-as-code and automated deployment.
* https://drive.google.com/file/d/1y6zlMSbHz6bYDskpxZ1HSP9SUgO2qS-y/view?usp=sharing


***Conclusion***
Project Scarecrow provides farmers with a scalable, secure, and humane solution to scare away pests using IoT, machine learning, and AWS services. It complies with industry standards and provides real-time insights to enhance farm protection globally.