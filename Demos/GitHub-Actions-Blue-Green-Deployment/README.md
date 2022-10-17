# Blue Green Deployment Strategy using GitHub Actions

## Description

This demo uses GitHub **Actions** and **Azure App Services** to show case how to deploy an application using blue green deployment strategy.

## Demo Features

- GitHub Actions
- Azure App Services
- Docker container
- Azure Bicep
- GitHub CLI

## Prerequisites

You will need an active GitHub account and Azure subscription. Install the following tools too:

- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)
- [GitHub CLI](https://github.com/cli/cli#installation)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Optional

If you want to demo manual approval create an environment on your repository and assign yourself as approver. If you're not familiar with the concept, [follow these instructions on this blog post](https://devblogs.microsoft.com/devops/i-need-manual-approvers-for-github-actions-and-i-got-them-now/).

## Before the class

First replace the values of these three variables in the `run.azcli` script in the `.scripts` folder:

- `LOCATION="<REGION>"`
- `SUBID="<SUBSCRIPTION_ID>"`
- `GITHUB_ORGNAME="<ORG_NAME>"`

Then run the commands in `run.azcli` up to line #13. Capture the output of the last command and use it to create a secret in your GitHub repository called `AZURE_CREDENTIALS`. Create another secret for the name of the resource group called `AZURE_RG`.

## During the class

Copy the content of the folder into a new folder and get rid of the git files. Then run the script from line #15 to #27.

> **Note**: If you have closed your terminal you need to run the first few lines to create the variables again.

Once the files are pushed up, there will be a new workflow triggered and an App Service Plan, App Service, and a Container Registry will get created in your resource group.

At this point you need to create three more secrets in your GitHub repository:

- `REGISTRY_LOGIN_SERVER`
- `REGISTRY_USERNAME`
- `REGISTRY_PASSWORD`

You can run the script from line #29 onwards.

Now trigger the deploy action and walk the learners through what is happening. In a nutshell we're deploying to the staging slot first, then validate and swap it with production.
