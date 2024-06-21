# Terraform IaC Multi-Cloud Repository
This repository contains the infrastructure as code (IaC) configurations for managing and provisioning resources across multiple environments (SIT, UAT, PROD) and cloud providers (AWS, Google Cloud).

## Repository Structure
This repository is organized to support multiple projects, each with its own set of requirements. The directory structure is designed to promote clarity, maintainability, and scalability.

## Directory Overview
environments/: Contains the different environments (SIT, UAT, PROD).

sit/, uat/, prod/: Each environment folder contains subfolders for each project.
project-a/, project-b/: Each project folder contains subfolders for each cloud provider.
aws/, google/: These folders contain the main Terraform configurations for each cloud provider, including specific service configurations (e.g., S3, Athena, IAM user for AWS; BigQuery, GCS, IAM user for Google).
modules/: Contains reusable Terraform modules for both AWS and Google Cloud.

aws/, google/: Each cloud provider has subfolders for different types of modules (e.g., network, compute, S3, Athena, IAM user for AWS; network, compute, BigQuery, GCS, IAM user for Google).
shared/: Contains shared configurations such as provider setup, version constraints, and backend configuration.

```css
terraform-iac-repo/
├── README.md
├── environments/
│   ├── sit/
│   │   ├── project-a/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
│   │   ├── project-b/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
│   ├── uat/
│   │   ├── project-a/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
│   │   ├── project-b/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
│   ├── prod/
│   │   ├── project-a/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
│   │   ├── project-b/
│   │   │   ├── aws/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── s3.tf
│   │   │   │   ├── athena.tf
│   │   │   │   ├── iam_user.tf
│   │   │   ├── google/
│   │   │   │   ├── main.tf
│   │   │   │   ├── variables.tf
│   │   │   │   ├── outputs.tf
│   │   │   │   ├── bigquery.tf
│   │   │   │   ├── gcs.tf
│   │   │   │   ├── iam_user.tf
├── modules/
│   ├── aws/
│   │   ├── network/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── compute/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── s3/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── athena/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── iam_user/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   ├── google/
│   │   ├── network/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── compute/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── bigquery/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── gcs/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
│   │   ├── iam_user/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   ├── outputs.tf
└── shared/
    ├── provider.tf
    ├── versions.tf
    ├── backend.tf
```
