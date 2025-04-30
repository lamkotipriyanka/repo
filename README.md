# CDO Data Engineering
##### THIS REPOSITORY WILL FOLLOW THE [MST BRANCHING STRATEGY](https://github.com/colpal/MST-branching)

## 📑 Table of Contents

1. [Important Links](#important-links)
2. [Installing and Setting Up VS Code](#installing-and-setting-up-vs-code)
3. [What is `master` and `develop`](#what-is-master-and-develop)
4. [Branch Naming Conventions](#branch-naming-conventions)
5. [How to Create a New Master Branch](#how-to-create-a-new-master-branch)
6. [How to Merge Your Local Branch with `develop`](#how-to-merge-your-local-branch-with-develop)
7. [How to Merge Your Local Branch with `master`](#how-to-merge-your-local-branch-with-master)
8. [How to Resolve Conflicts](#how-to-resolve-conflicts)


---

## 🔗 Important Links :
| Airflow Environment | GCP Environment | Snowflake Environment |
| :-----------------: | :-------------: | :--------------------:|
| [DEV](https://dev-cdo-data-engineering.airflow.colpal.cloud) | [DEV](https://console.cloud.google.com/home/dashboards?project=cp-saa-internal-sales-dev) | [DEV](app.snowflake.com/colpal/colgatepalmolivedev/#/homepage) |
| [PROD](https://prod-cdo-data-engineering.airflow.colpal.cloud) | [PROD](https://console.cloud.google.com/home/dashboards?project=cp-saa-internal-sales-prod) |[PROD](app.snowflake.com/colpal/colgatepalmoliveprod/#/homepage) |

## 📍 Installing and Setting Up VS Code 
To install and set up Visual Studio Code (VS Code) on your laptop, you can follow these steps:
Download and Install VS Code:
Visit the official VS Code website:[VS CODE](https://code.visualstudio.com)
Download VS Code
.
Choose the version suitable for your operating system (Windows, macOS, or Linux) and download the installer.
Follow the installation instructions to complete the setup.

## 🌳 What is master and develop
master: Main production-ready branch. Only stable and tested code goes here.

develop: Active development branch where features are merged before going to master.

## 📌 Branch Naming Conventions :
Use Lowercase Letters: Only use lowercase letters in branch names. 
Separate Words with Hyphens: Use hyphens (-) to separate words, making the branch name easily readable.
Inclusion of project name: Use a prefix like project-name/ to help us identify the project, followed by a concise description of the feature / bug you're working on, e.g., smile-store/vn-email-alert
No Special Characters or Spaces: Avoid using spaces or special characters. Stick to alphanumeric characters and hyphens for separating words.
Be Descriptive but Concise: Branch names should give enough context about the purpose of the branch but should remain concise.

## 🆕 How to Create a New Master Branch :
1. Checkout master branch : git checkout master 
2. Pull the latest changes : git pull origin master 
3. Create a new branch from master : git checkout -b new-master-branch

## 🌿 How to merge your local branch with develop :
1. Create a new master branch and make the changes in the code.
2. Add and commit them -
   git add .
   git commit-m "Description of your change"
3. Switch to the develop branch : git checkout develop 
4. Pull the latest changes from develop: git pull origin develop
5. Merge your feature branch into develop: git merge feature/your-branch-name
6. Resolve any merge conflicts if prompted (see How to Resolve Conflicts).
7. Push the updated develop branch to the remote repo: git push origin develop

## ✍️ How to merge your local branch with master :
1. Create a new master branch , make changes in the code
2. Add and commit them -
   git add. ,
   git commit -m "Description of your change"
3. Switch to the master branch and update the master branch :
   git checkout master ,
   git pull origin master
4. Merge the local branch into the master - git merge your-local-branch
5. Push the updated branch to the Repository - git push 

## ⚙️ How to Resolve Conflicts :
1. Checkout your own branch: git checkout <your-branch>
2. Create and switch to a new conflict branch: git checkout -b conflict-branch
3. Checkout and update to your local the develop branch:
git checkout develop
git pull origin develop
4. Switch back to your conflict-branch (opens branch in your local): git checkout conflict-branch
5. Merge the develop branch into the conflict-branch: git merge develop
6. Resolve any conflicts that arise:
7. Open the files with conflicts using your preferred text editor.
   Amend the conflicting code sections and save the changes.
8. Commit the resolved changes: git commit -m "Resolved merge conflicts"
9. Push the conflict-branch to the remote repository: git push -u origin conflict-branch

Create a Pull Request (PR) using the conflict branch:
Navigate to your repository on the Git platform (e.g., GitHub, GitLab).
Start a new pull request, selecting conflict-branch as the source branch and develop as the target branch.

