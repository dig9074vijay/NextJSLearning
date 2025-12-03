# GitHub Pages Setup Instructions

This project is now configured to automatically deploy the Playwright test report to GitHub Pages after each successful test run on the main branch.

## Steps to Complete Setup

1. **Enable GitHub Pages in Repository Settings:**

   - Go to your repository on GitHub
   - Navigate to Settings > Pages
   - Under "Source", select "GitHub Actions"
   - Save the settings

2. **Workflow Configuration:**
   The GitHub Actions workflow (`.github/workflows/playwright.yml`) has been updated to:

   - Run Playwright tests
   - Build and upload the test report as an artifact
   - Deploy the report to GitHub Pages (only on main branch)

3. **Accessing Your Site:**
   After the workflow runs successfully, your Playwright test report will be available at:

   ```
   https://<your-username>.github.io/<repository-name>/
   ```

   For your repository, it should be:

   ```
   https://dig9074vijay.github.io/NextJSLearning/
   ```

## What Gets Deployed

- The Playwright test report (`playwright-report/` directory)
- Interactive HTML report with test results, screenshots, and traces
- Accessible directly in the browser without downloading

## Workflow Triggers

The deployment will happen automatically when:

- Code is pushed to the `main` branch
- Tests pass successfully
- The workflow completes without errors

## Notes

- Only pushes to the main branch trigger deployment
- Pull requests will run tests but won't deploy
- The site updates automatically on each successful test run
- Test reports from different runs will overwrite previous ones
