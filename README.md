



# Create your first pipeline

This is a step-by-step guide to using Azure Pipelines to set up continuous integration for a GitHub repository.

## Prerequisites

* You'll need a **GitHub account**, where you can create a repository.
* You'll need a **Microsoft account**, otherwise known as a Live ID. If you already have one, such as a personal email address you use to sign into Windows at school or home, you can use it. Otherwise, [create a new one](https://signup.live.com/signup/).

## Fork the Universe repository

1. Sign into your personal GitHub account by clicking **Sign in** at the top-right of this page.
1. Click **Fork** at the top-right of this page.
1. Choose your personal GitHub account where the repository will be forked. GitHub will fork the repository and navigate to it in your account.

## Install the Azure Pipelines GitHub App

1. Browse to https://github.com/apps/azure-pipelines and click **Install** (or Configure).
1. Click the name of your GitHub account into which the repository was forked. Then click **Install**.
1. After you're redirected to Azure DevOps, sign in with your Microsoft account (see [Prerequisites](#Prerequisites)).
1. If you see a drop-down labeled "Select your Azure DevOps organization," then click **Create a new organization** below it.
1. Click **Continue**. An Azure DevOps organization will be created for you that is linked to your GitHub account's repositories.

## Create a new pipeline

1. After you're redirected to the "New pipeline" page of your Azure DevOps organization, select your `Universe` repository fork to create a pipeline for it.
1. Select the **Docker image** template to build the repo's Dockerfile. Or, for an npm-only build, select **Node.js**.
1. YAML text that defines your pipeline will be displayed. To build your repository on a different OS, change the **vmImage** value from `'Ubuntu 16.04'` to:
    * `'macOS-10.13'` for macOS, or
    * `'vs2017-win2016'` for Windows
1. Click **Save and run**. In the pane that appears, select **Create a new branch for this commit and start a pull request**. Then, click **Save and run** at the bottom of the pane.
1. The YAML file is pushed to a new branch of your GitHub repository, a pull request is created for it, and you'll see the pipeline run for the first time.

    #### You did it! Congratulations!

## Optional next steps

You've just learned the basics of using Azure Pipelines. Consider trying these follow-on steps.

### Check your build results in GitHub

1. Navigate to your repository fork in your GitHub account (ex: `https://github.com/janedoe/Universe`).
1. Click the **Pull requests** tab and select the pull request that was created for you, named **Set up CI with Azure Pipelines**.
1. At the bottom of the page, click **Show all checks** to see the build status of your pipeline.
1. Near the top of the page, click the **Checks** tab. Select your build under the **Azure Pipelines** section to see more status information. To view detailed logs or manage your pipeline, click **View more details on Azure Pipelines**.

### Add the status badge to your repository

1. In Azure Pipelines, go to the **Builds** page to view the list of pipelines.
1. Select the pipeline that was created for you.
1. In the context menu for the pipeline, select **Status badge**.
1. Copy the **Sample Markdown** text to the clipboard.
1. Paste the Markdown at the top of your repository's `README.md` file.

### Create another pipeline

Create additional pipelines by clicking **+ New build pipeline** from within Azure Pipelines.

### Deploy

Ask an Azure Pipelines representative how you can deploy your application to any platform or cloud.
