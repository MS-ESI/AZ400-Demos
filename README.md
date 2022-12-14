# AZ400-Demos

This repository will host demos that MTTs will be able to use. The following points will explain the base structure and instructions to use and collaborate on the hosted demos.

# DEMOS available

1. [GitHub Packages CICD for Nuget using GitHub Actions and GitVersion](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/GitHub-Packages-CICD-Nuget) @unaihuete
    - External Public Repo Demo: https://github.com/unaihuete-org/nuget_CICD
1. [Blue Green Deployment Strategy using GitHub Actions](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/GitHub-Actions-Blue-Green-Deployment) @yashints
1. [Azure Bicep Local Deployment with Key Vault](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/Azure-Bicep-Local-Deployment) @yashints
1. [Using variables in GitHub Actions](https://github.com/massimobonanni/VariablesInActions) @massimobonanni
1. [GitHub packages for npm using GitHub Actions](Demos/GitHub-Packages-CICD-NPM) @yashints
1. TODO App Configuration + Key Vault @fimdim

## Repo Structure

- **Demos** folder will hold each demo folder+files. **Give a significant name to your demo folder**.
- **README** file explain the main guidelines of the repository and an index with the offered demos for quick access.
- **CODEOWNERS** file defines the people responsible to review updatesIssues related to the hosted demos (GitHub includes the owner as automatic reviewer on the opened Pull Requests)

### DEMO folder structure

The mentioned folders are used depending on functionality needed:

- **.ado** folder should contain the ADO pipelines (**YAML** preferred, classic ones could be hosted exported and hosted as JSON)
- **.azure** folder should contain **Bicep/ARM** files.
- **.scripts** folder should contain **PS/Bash** or any scripts used on the demo.
- **.github** folder will contain github specific files, like **YAML** worfklows (under **.github/workflow** folder)
- **src** folder should contain application related code
- **README.md** file should contain demo guidance and demonstrated features list (TODO: use this one as an example)

## Creating a DEMO

### OPTION 1 Reference your external demo

Add a reference to your own **public** repository on this README.md file [here](#demos-available). **Try to keep the reference [folder structure](###demo-folder-structure) and complete README file**.

Add your @GH-account next to your demo (so that people know who to reach for help)

### OPTION 2 Import your demo 

A demo template repository will be given to use as an starting base : https://github.com/MS-ESI/DEMO-Template . Use it as a template for you demo, feel free to delete folder/files not needed. **Maintain the structure**

Once your demo has the previosly mentioned structure, in order to import it to AZ-400-Demos repo:
1.create a branch for your changes
2.create a demo folder (meaningful name) under **DEMOS** and upload those files 3. Modify the CODEOWNERS file in the root of the repo, assign yourselve as maintainer (to review related PRs). 3. Create a PR for us to review it and include your demo

## Using a DEMO (TODO)
