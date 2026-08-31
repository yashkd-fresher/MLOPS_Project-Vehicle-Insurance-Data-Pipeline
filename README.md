Vehicle Insurance Data Pipeline — MLOps Project

An end-to-end, modular machine learning pipeline for vehicle insurance data — covering ingestion, validation, transformation, training, evaluation, and deployment — with MongoDB Atlas as the data source, AWS (S3, EC2, ECR) for the model registry and hosting, Docker for containerization, and GitHub Actions for CI/CD.

MongoDB Atlas
     │
     ▼
Data Ingestion → Data Validation → Data Transformation → Model Trainer
                                                                │
                                                                ▼
                                            Model Evaluation → Model Pusher (AWS S3)
                                                                │
                                                                ▼
                                                  Prediction Pipeline (Flask app)
                                                  
                                                  
Every stage follows the same pattern: constants → configuration → data access → entity (config/artifact) → component → pipeline integration, with structured logging and custom exception handling throughout.

Tech Stack
Language: Python 3.10
Data store: MongoDB Atlas
Cloud: AWS (S3, EC2, ECR, IAM)
Containerization: Docker
CI/CD: GitHub Actions (self-hosted EC2 runner)
Serving: Flask
