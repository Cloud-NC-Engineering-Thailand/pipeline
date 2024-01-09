# Building and Deploying applications to Google Cloud Runs

With this particular workflow focused on deploying applications to Google Cloud Run. The workflow is triggered on pushes to the `develop` branch.

## Workflow Description
The `Deploy Cloud Run to Dev Environment` workflow consists of several steps:
1. **Authentication** : Authenticates with Google Cloud using the provided credentials.
2. **Set up Cloud SDK** : Sets up Google Cloud SDK with the specified project ID and exports default credentials.
3. **Build and Push Image to GCP Artifact Registry** : Builds the Docker image and pushes it to the specified Container Registry URL.
4. **Deploy on Cloud Run** : Deploys the image to Google Cloud Run on the specified target service, port, region, and with the given service account.


## Usage
To utilize this workflow:

1. Define the required inputs in your GitHub repository's secrets or in the workflow file.
2. Place this workflow file in your repository under `.github/workflows`.
3. Trigger the workflow based on your GitHub Actions settings (e.g., on push, pull request, or manually).

This workflow streamlines deploying applications to Google Cloud Run by automating various operations, ensuring consistency and reducing the likelihood of errors in deployments.

## Inputs
- `GCP_CREDENTIALS`: Google Cloud credentials JSON (required).
- `GOOGLE_PROJECT`: Google Cloud project ID (required).
- `CR_URL`: Container Registry URL (required).
- `ARTIFACT_FOLDER`: Artifact folder in the container registry (required).
- `IMAGE_NAME`: Image name (required).
- `TARGET_SERVICE`: Target service for deployment (required).
- `PORT`: Port number (required).
- `REGION`: Google Cloud region (required).
- `SA_MAIL`: Service account email (required).

## Usage Examples (For CloudNC Dev)
### **You can see the example of The caller repo that call this workflows [Here](https://github.com/Cloud-NC-Engineering-Thailand/test-use-pipeline)**
