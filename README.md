# AZ400-Demos

This repository will host demos that MTTs will be able to use. The following points will explain the base structure and instructions to use and collaborate on the hosted demos.

# DEMOS available

1. [GitHub Packages CICD for Nuget using GitHub Actions and GitVersion](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/GitHub-Packages-CICD-Nuget) @unaihuete
1. [Blue Green Deployment Strategy using GitHub Actions](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/GitHub-Actions-Blue-Green-Deployment) @yashints
1. [Azure Bicep Local Deployment with Key Vault](https://github.com/MS-ESI/AZ400-Demos/tree/main/Demos/Azure-Bicep-Local-Deployment) @yashints

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

A demo template repository will be given to use as an starting base : https://github.com/MS-ESI/DEMO-Template . Use it as a template for you demo, feel free to delete folder/files not needed. **Maintain the structure**

Once your demo has the previosly mentioned structure, in order to import it to AZ-400-Demos repo:
1.create a branch for your changes
2.create a demo folder (meaningful name) under **DEMOS** and upload those files 3. Modify the CODEOWNERS file in the root of the repo, assign yourselve as maintainer (to review related PRs). 3. Create a PR for us to review it and include your demo

## Using a DEMO (TODO)

There are two ways to use the demos:

1. Download the repository and just use the selected demo folder files.
2. Using Git commands, clone just a folder, using `sparse-checkout`, example:

   1. From you terminal: `git clone --no-checkout https://github.com/MS-ESI/AZ400-Demos`
