# Multi-Tier Web Application on AWS

This repository showcases a fully deployed multi-tier web application hosted on AWS. The project demonstrates the use of scalable and highly available cloud architecture to build modern web applications.

---

## Project Overview
The Multi-Tier Web Application is a robust architecture designed to separate different components of an application, ensuring scalability, fault tolerance, and high availability. The project utilizes AWS services to deploy a web application with the following tiers:

1. **Frontend Tier**: Hosted static assets on AWS S3 with CloudFront for global content delivery.
2. **Backend Tier**: Deployed a dynamic API using AWS Elastic Beanstalk.
3. **Database Tier**: Configured a relational database using Amazon RDS.

---

## Architecture Diagram
```
Browser --> CloudFront --> S3 (Static Content)
                  |
                  --> Elastic Load Balancer --> Elastic Beanstalk (EC2)
                                               |
                                               --> Amazon RDS (Database)
```

---

## Features
- **High Availability**: Application Load Balancer ensures traffic distribution across multiple instances.
- **Scalability**: Auto Scaling groups adjust the number of backend instances based on demand.
- **Secure Architecture**: SSL encryption via CloudFront and IAM role-based access controls.
- **Cost Optimization**: Leverages S3 and CloudFront for low-cost content delivery.
- **Monitoring**: AWS CloudWatch for performance metrics and alerts.

---

## Technologies Used
- **Frontend**: AWS S3, CloudFront
- **Backend**: Elastic Beanstalk, EC2, Load Balancer
- **Database**: Amazon RDS (MySQL)
- **Monitoring**: AWS CloudWatch
- **Automation**: CI/CD pipeline with GitHub Actions

---

## Prerequisites
1. AWS Account
2. AWS CLI installed and configured
3. Domain name (optional, for custom DNS)

---

## Setup Instructions

### Step 1: Configure S3 Bucket
1. Create an S3 bucket for hosting static files.
2. Enable static website hosting.
3. Upload your frontend files (HTML, CSS, JS).
4. Configure bucket policies for public read access.

### Step 2: Deploy Backend to Elastic Beanstalk
1. Package your backend application (Node.js, Python, etc.).
2. Deploy it to Elastic Beanstalk using the AWS Management Console or CLI.
3. Configure Auto Scaling and Load Balancer settings.

### Step 3: Configure RDS Database
1. Create an Amazon RDS instance (MySQL/PostgreSQL).
2. Configure security groups to allow access from the backend instances.
3. Update backend application configurations with RDS connection details.

### Step 4: Setup CloudFront Distribution
1. Create a CloudFront distribution.
2. Set the S3 bucket as the origin.
3. Configure SSL/TLS certificates for secure connections.

---

## CI/CD Pipeline (Optional)
1. Set up GitHub Actions to automate deployments to Elastic Beanstalk and S3.
2. Use AWS CLI in pipeline scripts for deployments.

---

## Monitoring and Alerts
1. Configure AWS CloudWatch to monitor application health.
2. Set up alarms for key metrics (e.g., CPU utilization, latency).
3. Integrate alarms with SNS for email/SMS notifications.

---

## Future Improvements
- Implement serverless options using AWS Lambda and API Gateway.
- Add caching for database queries with Amazon ElastiCache.
- Enable logging and analysis using AWS CloudTrail.

---

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to enhance this project.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact
**Praise Ajanaku**  
Email: [praiseajanaku@gmail.com](mailto:praiseajanaku@gmail.com)  
LinkedIn: [linkedin.com/in/praise-ajanaku](https://linkedin.com/in/praise-ajanaku)
