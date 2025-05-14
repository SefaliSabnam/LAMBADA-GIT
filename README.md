# LAMBADA-GIT

This repository demonstrates the setup and deployment of an AWS Lambda function using GitHub Actions for CI/CD.

## Project Structure

```
LAMBADA-GIT/
├── .github/
│   └── workflows/
│       └── lambda.yaml        # GitHub Actions workflow for AWS Lambda deployment
├── src/
│   └── lambda_function.py     # Lambda function source code
└── README.md                  # Project documentation (this file)
```

## Features

* AWS Lambda function deployment using GitHub Actions.
* Automated deployment on each push to the main branch.

## Prerequisites

* AWS Account
* GitHub Account
* AWS CLI configured
* Git installed

## Setup

1. Clone the repository:

   ```bash
   git clone <repository_url>
   cd LAMBADA-GIT
   ```

2. Set up your AWS credentials in GitHub as Secrets:

   * `AWS_ACCESS_KEY_ID`
   * `AWS_SECRET_ACCESS_KEY`
   * `AWS_REGION` (e.g., ap-south-1)

3. Review the `.github/workflows/lambda.yaml` file for the CI/CD configuration.

## Understanding the Workflow

* The GitHub Actions workflow (`lambda.yaml`) triggers on every push to the main branch.
* It performs the following steps:

  * Sets up AWS CLI.
  * Packages the Lambda function.
  * Deploys the function to AWS Lambda.

## Deployment

To manually deploy the Lambda function:

1. Make changes to `src/lambda_function.py`.
2. Commit and push the changes to the `main` branch.
3. The GitHub Actions workflow will automatically deploy the updated function.

## Lambda Function

The Lambda function (`lambda_function.py`) is a simple example. Customize this file based on your application logic.

## Author

* **Sefali Sabnam**

