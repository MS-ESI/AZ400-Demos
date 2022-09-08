# GitHub Packages CICD for Nuget using GitHub Actions and GitVersion

## Description

The following repo demonstrates how to integrated GitHub Action with GitHub Packages for continuous delivery of Nuget Packages. By Using GitVersion, packages will be automatically versioned depending on the git history and branch triggering the workflow (gitversion.yml file defines this settings). 
## Demo Features
- GitHub Actions
- GitHub Packages
- Nuget
- GitVersion (https://gitversion.net/) for automatic versioning

## Demo Guide

Once you have imported/copied the demo folder files, you need to follow the next steps:

1. In **src/EShopWeb.Shared/EShopWeb.Shared.csproj** change the **RepositoryUrl** to your own repository.
2. **Create an Github PAT** to allow your workflow to publish the package to GitHub Packages. Create a PAT following the steps defined in this link and adding at least ```write:packages``` permissions: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

   >NOTE: GITHUB_TOKEN could also be used.

3. Create a repository secret called **PAT_GH_PACKAGES** hosting the previously created PAT.
4. In **.github/workflow/nuget-cicd.yml**, line 45, replace **unaihuete-org** with your own GitHub organization name.
5. Make a change to the **master** branch or a **feature/*** branch a wait for the workflow execution. Master branches will create a clean version numbered package, while feature branches will contain an 