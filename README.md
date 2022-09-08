# AZ400-Demos
This repository will host demos that MTTs will be able to use. The following points will explain the base structure and instructions to use and collaborate on the hosted demos.

# DEMOS available

1. (GitHub Packages CI/CD for Nuget using GitHub Actions and GitVersion for automatic versioning) []
## Repo Structure

- **Demos** folder will hold each demo folder+files. **Give a significant name to your demo folder**.
- **README** file explain the main guidelines of the repository and an index with the offered demos for quick access.
- **CODEOWNERS** file defines the people reponsible to review updates related to the hosted demos (GitHub includes the owner as automatic reviewer on the opened Pull Requests)

###  DEMO folder structure 
The mentioned folders are used depending on functionality needed:
- **.ado** folder should contain the ADO pipelines (**YAML** preferred, classic ones could be hosted exported and hosted as JSON)
- **.azure** folder should contain **Bicep/ARM** files.
- **.scripts** folder should contain **PS/Bash** or any scripts used on the demo.
- **.github** folder will contain github specific files, like **YAML** worfklows (under **.github/workflow** folder)
- **src** folder should contain application related code
- **README.md** file should contain demo guidance and demonstrated features list (TODO: use this one as an example)

### DEMO template
A demo template repository will be given to use as an starting base. 