# Data-Science-With-R

## Markdown Cheatsheet

A Markdown Cheatsheet can be found at [https://www.markdownguide.org/cheat-sheet/](https://www.markdownguide.org/cheat-sheet/)

## Get Started With GitHub

The Hello World Exercise: [https://docs.github.com/en/get-started/quickstart/hello-world](https://docs.github.com/en/get-started/quickstart/hello-world)

### Steps

1. **Create a repository** with a README file.
2. **Create a branch** off your main branch. A branch is a copy of main at the time the branch is made. Edits can be done to the branch and when the edits are complete, the branch can be merged into main. Name the new branch readme_edits
3. **Make and commit changes** to the README.md file in the readme_edits branch. Use various Markdown elements (see cheatsheet link above).
4. **Open a pull request.** This means: you propose your changes and request that someone review them and merge them into their branch. Pull requests show diffs, or differences, of the content from both branches. The changes, additions, and subtractions are shown in different colors.

### Pull request

1. Under **Pull requests tab** of your repository, click **New pull request**.
2. In the Example Comparisons Box, select the branch with the edits you want to review and merge. Review the changes. Click **Create pull request**. Collaborators can now review edits and make suggestions.
3. **Merge pull request**.
4. **Delete branch**.

## Set up Git

Instructions: [https://docs.github.com/en/get-started/quickstart/set-up-git](https://docs.github.com/en/get-started/quickstart/set-up-git)

1. Install Git

Git comes with XCode
Type in Terminal to see Git version: git --version

Type in Terminal to get latest version: git clone https://github.com/git/git

2. Set your username in Git: mimsbims
3. Set your commit email address in Git

If you'd like to keep your personal email address private, you can use a noreply email address from GitHub as your commit email address.
6374386+mimsbims@users.noreply.github.com

## Tutorial: creating R Markdown documents with RStudio and publishing them via GitHub using GitHub Pages

The tutorial is at [https://resources.github.com/github-and-rstudio/](https://resources.github.com/github-and-rstudio/). Some of the instructions did not work for me and I had to do a few extra steps to get them to work. I documented the extra steps below.

### Clone the repository with RStudio

In the Code tab of your GitHub repository, click on Code (green button with down arrow). Copy the https URL for your repository.

For more details on cloning a repository:
[https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#about-cloning-a-repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#about-cloning-a-repository)

In RStudio: New Project -> Version Control -> Git

### Create an R Markdown document in RStudio

No issues with these instructions

### Commit and push the changes to GitHub

**5. Click Commit** - This failed. Needed to use "git add filename" to add new file to repo.

In Terminal:

```console
cd project_directory
git add new_file
```
After doing that, click Commit worked.

**6. Pull** (to fetch remote changes) - This failed. Fatal: Need to specify how to reconcile divergent branches.

Note: I had edited README.md in GitHub.com and committed the edits after cloning the repository with RStudio.

Fix: Pull button in RStudio has a drop down arrow. I clicked **Pull with rebase** and that succeeded in pulling the changes from the remote repo.

**7. Push** (to push local changes to remote repo) - This failed. Support for pw auth. was removed on Aug 13, 2021. Auth. failed.

Fix: I installed **Git Credential Manager (GCM)**. I used homebrew in the Terminal, but it may have been easier to download the installation package. Homebrew took many minutes to upgrade.

More information about GCM can be found here: [Getting started with Git - Caching credentials](https://docs.github.com/en/get-started/getting-started-with-git/caching-your-github-credentials-in-git)

[Install instructions for GCM](https://github.com/GitCredentialManager/git-credential-manager/blob/release/docs/install.md)





