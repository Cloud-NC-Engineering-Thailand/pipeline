# Deploying applications to Google Cloud Runs

With this particular workflow focused on deploying applications to Google Cloud Run. The workflow is triggered on pushes to the `develop` branch.

## Workflow Description
The `Deploy Cloud Run to Dev Environment` workflow consists of several steps:
1. **Checkout Source Code**: Checks out the code for the workflow.
2. **Config GCP Auth**: Sets up Google Cloud authentication.
3. **Prepare GCP Auth to GCP Artifactory**: Configures Docker to use gcloud as a credential helper.
4. **Set up GCP Cloud SDK**: Sets up the Google Cloud SDK.
5. **Build and Push Container Image to GCP Artifactory**: Builds the Container image and pushes it to Google Artifactory.
6. **Deploy the image to Cloud Run**: Deploys the Container image to Google Cloud Run.

## Usage
To use this workflow in your project:
1. Ensure you have the necessary secrets (`GCP_CREDENTIALS`) set in your GitHub repository.
2. Customize the environment variables as needed (`GOOGLE_PROJECT`, `CR_URL`, `SERVICE`, `REGION`).
3. Include this workflow in your repository and it will be triggered on push to the `develop` branch.