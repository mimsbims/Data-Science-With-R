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

1. File -> New File -> R Markdown (HTML output)
2. File -> Save (don't knit)
3. Add new file to staging area. 

If this step is skipped and one tries to commit the change, there will be an error message: nothing added to commit but untracked files present. There is a Terminal tab in RStudio in the bottom left, next to the Console tab. If it isn't there, click More in the menu for the Git window in RStudio, then click New Terminal.

In Terminal type:

```console
git add new_file
```

4. Click Commit 
5. Click Pull (to fetch remote changes)

If there were no changes to the remote repository since the last time the local and remote repositories were synched, you will get the message: already up to date. 

If there as been a change to the remote repository, you may get an error message: fatal: need to specify how to reconcile divergent branches. Try **Pull with rebase** instead (in dropdown menu for Pull button).

For more information on merging divergent branches see [the Pro Git book](https://git-scm.com/book/en/v2)

**7. Push** (to push local changes to remote repo) - This failed. Support for pw auth. was removed on Aug 13, 2021. Auth. failed.

Fix: I installed **Git Credential Manager (GCM)**. I used homebrew in the Terminal, but it may have been easier to download the installation package. Homebrew took many minutes to upgrade.

More information about GCM can be found here: [Getting started with Git - Caching credentials](https://docs.github.com/en/get-started/getting-started-with-git/caching-your-github-credentials-in-git)

[Install instructions for GCM](https://github.com/GitCredentialManager/git-credential-manager/blob/release/docs/install.md)





