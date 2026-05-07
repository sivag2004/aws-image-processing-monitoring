AWS Observability Image Processing Pipeline

This project demonstrates an end-to-end serverless image processing and observability system built on Amazon Web Services using Terraform.

It processes images uploaded to S3 and provides real-time monitoring, logging, and alerting to ensure system reliability and performance.

Architecture
<img width="1116" height="646" alt="Screenshot from 2026-05-07 22-02-56" src="https://github.com/user-attachments/assets/4a50e2ee-e911-4b0c-9b51-6b7f3686765a" />

Features
   Image upload triggers processing via AWS Lambda
   Image compression, format conversion (JPEG, PNG, WEBP), thumbnail generation
   Monitoring using Amazon CloudWatch
   Structured logging with Amazon CloudWatch Logs
   Real-time alerts using Amazon SNS

Architecture Flow
  Upload image to S3
  S3 triggers Lambda function
  Lambda processes the image
  Logs and metrics sent to CloudWatch
  Alerts triggered via SNS (Email)

Observability
  Custom Metrics
    Processing Time (ms)
    Images Processed
    Success / Failure Count

  Logs
    Request ID tracking
    Execution time
    Error tracing

  Alerts
    Email notification on failure or anomalies

  Tech Stack
    Amazon Web Services (S3, Lambda, CloudWatch, SNS)
    Terraform (Infrastructure as Code)
    Python (Boto3, Pillow)


How to Deploy
  cd terraform
  terraform init
  terraform apply

 Screenshots
   CloudWatch Dashboard
   <img width="2388" height="1282" alt="Screenshot from 2026-05-07 22-04-54" src="https://github.com/user-attachments/assets/edac5a51-2ec8-4638-a538-3c36271434c7" />

    
   Logs
   <img width="2388" height="1282" alt="Screenshot from 2026-05-07 22-05-55" src="https://github.com/user-attachments/assets/0ce98257-84bc-48f8-b626-d04dd9439e45" />


   Alert Email
   <img width="1600" height="858" alt="WhatsApp Image 2026-05-07 at 11 13 24 PM" src="https://github.com/user-attachments/assets/c6fb5959-9c19-4d47-a225-245616ebba93" />


Key Learnings
 Event-driven architecture (S3 → Lambda)
 Building observable systems (Logs + Metrics + Alerts)
 Serverless processing pipelines
 Real-time monitoring & alerting

Future Improvements
 Add auto-remediation using AWS Lambda
 Integrate Slack alerts
 Add CloudWatch dashboard enhancements
 Implement anomaly detection

Author
 Sivaganesh T
