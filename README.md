# GitHub Actions Experiment

This repository demonstrates the use of GitHub Actions for automating build and deployment workflows.

## Workflow Overview

The main workflow is defined in [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml). This workflow automates the process of building, testing, and deploying the application when changes are pushed to the `main` branch.

### Workflow Steps

1. **Build Job**
   - **Runs on:** `ubuntu-latest`
   - **Steps:**
     - Checks out the repository code.
     - Runs tests (replace the placeholder with your actual test commands).
     - Builds the application (replace the placeholder with your actual build commands).

2. **Deploy Job**
   - **Runs on:** `ubuntu-latest`
   - **Needs:** The `build` job to complete successfully.
   - **Environment:** `uat`
   - **Steps:**
     - Checks out the repository code.
     - Deploys the application to the server (replace the placeholder with your actual deployment commands, such as SSH or Docker).

This setup ensures that deployments only occur after a successful build and test process, and links the deployment to a specific environment for better control and visibility.