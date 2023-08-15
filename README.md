# Serverless Application CI/CD

This repository contains the setup for continuous integration and continuous deployment (CI/CD) of a Serverless Application using GitHub Actions.

## Overview

The purpose of this project is to automate the process of building, testing, and deploying a Serverless Application using GitHub Actions. The workflow is triggered on each push to the repository, targeting the `main` branch. The workflow consists of the following steps:

1. **Pre-Deploy**: Check the event that triggered the workflow and display a message.

2. **Install Dependencies**: Checkout the repository code and install project dependencies using npm.

3. **Unit Testing**: Run unit tests on the Serverless Application using testing frameworks like Jest and Mocha.

4. **Deployment**: Deploy the Serverless Application to AWS Lambda using the Serverless Framework.

## Workflow Steps

The workflow is defined in the `.github/workflows/main.yml` file. Here's a brief explanation of each step:

- **Pre-Deploy**: Display a message indicating the event that triggered the workflow.

- **Install Dependencies**: Checkout the repository code and install project dependencies using `npm install`.

- **Unit Testing**: Checkout the code again, install dependencies, and run unit tests using testing frameworks.

- **Deployment**: Checkout the code, set up Node.js environment, install dependencies, and deploy the Serverless Application to AWS Lambda using the Serverless Framework.

## Getting Started

To use this CI/CD workflow for your own Serverless Application:

1. Fork this repository.

2. Update the Serverless Application code and tests in the appropriate directories.

3. Set up AWS credentials as repository secrets:
   - `AWS_ACCESS_KEY_ID`: Your AWS access key ID.
   - `AWS_SECRET_ACCESS_KEY`: Your AWS secret access key.

4. Make any necessary adjustments to the workflow configuration to match your project structure and requirements.

5. Push changes to your forked repository to trigger the workflow.


