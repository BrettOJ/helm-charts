# helm-charts
helm charts repository for github pages

# To Publish the Helm charts into the GitHub pages follow the steps below:

After making changes to the Helm repo in Github. follow the steps below to update the published location of the Help Chart
# 1. Git clone the chart you want to add to the Helm Repo 

# 2. Package the Helm Chart
# Index the Helm Repo 
helm repo index --url https://brettoj.github.io/helm-charts/ .

## Chat GPT Generated ReadMe

# Creating a Helm Chart Repository and Publishing to GitHub Pages

This guide outlines the steps to create a Helm chart repository and publish it using GitHub Pages.

## Step 1: Create a New GitHub Repository

1. Create a new GitHub repository.
2. Clone the repository to your local machine.

    ```bash
    git clone git@github.com:USERNAME/REPO_NAME.git
    ```

## Step 2: Create a Helm Chart

1. Create a new Helm chart or use an existing one.

    ```bash
    helm create my-chart
    ```

2. Modify the `my-chart` directory to fit your application needs.

## Step 3: Package the Helm Chart

1. Package the Helm chart into a `.tgz` file.

    ```bash
    helm package my-chart
    ```

    This will create a file like `my-chart-0.1.0.tgz`.

## Step 4: Create an `index.yaml` File

1. Initialize the repository by creating an `index.yaml` file.

    ```bash
    helm repo index .
    ```

## Step 5: Commit and Push

1. Add all files to your local git repository.

    ```bash
    git add .
    ```

2. Commit the files.

    ```bash
    git commit -m "Initial Helm Chart Repository"
    ```

3. Push the changes to GitHub.

    ```bash
    git push origin main
    ```

## Step 6: Set up GitHub Pages

1. Go to the Settings tab of your GitHub repository.
2. Scroll down to the GitHub Pages section.
3. Choose the branch you want to serve your Helm repository from (usually `main` or `gh-pages`).
4. Save the changes.

## Step 7: Test the Repository

1. Add the new chart repository to Helm.

    ```bash
    helm repo add my-helm-repo https://USERNAME.github.io/REPO_NAME
    ```

2. Update Helm repositories.

    ```bash
    helm repo update
    ```

3. Search for your Helm chart.

    ```bash
    helm search repo my-helm-repo
    ```

4. Install the chart.

    ```bash
    helm install my-release my-helm-repo/my-chart
    ```

## Additional Steps for Updates

Whenever you update a chart:

1. Repackage the chart.

    ```bash
    helm package my-chart
    ```

2. Update `index.yaml` file.

    ```bash
    helm repo index --merge index.yaml .
    ```

3. Commit and push changes to GitHub.

You should now have a Helm chart repository hosted on GitHub Pages.


