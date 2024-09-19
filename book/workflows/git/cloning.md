# Cloning a Repository

This page will show you how to use Source Control in VS Code to **clone** a repository. **Cloning** is the process of duplicating not only the files to your own computer, but also the record of all changes that have been made to those files in the past (that's what the git software is doing!). Because the history of these files is preserved, even if we make changes to these files in one of the repositories, the git software will provide a way to update the other software some time in the future. This allows multiple people to work on the same files at the same time; or, you as an individual to work on the same files using several different computers (e.g., a work and home laptop).

## Opening the Source Control tab in VS Code

Upon opening VS Code, we see that the first thing that is needed is to clone a repository ({numref}`clone1`). First, we have to get the address from our GitHub account.

```{figure} images/clone1.png
---
width: 80%
name: clone1
---
Opening the VS Code Source Control tab for the first time--we need to clone a repository.
```

Visit the repository you would like to clone to your computer on GitHub. As illustrated in {numref}`clone2`, you can see a bright green button "Clone" on the home page of the repository.

```{figure} images/clone2.png
---
width: 80%
name: clone2
---
Home page of the repository in GitHub; note the "Clone" button.
```

## Get the SSH address

To clone the repository, we need the address--its location on the internet. There are several ways to do this, but the most secure is using SSH. As illustrated in {numref}`clone3`, under "Clone with SSH," click the icon to copy the URL to your clipboard, then go back to VS Code.

```{figure} images/clone3.png
---
width: 40%
name: clone3
---
Copy SSH address of repository to your clipboard.
```

% Mona stopped here
## Set the local path

Now you are ready to click the "Clone Repository" option in the Source Control tab of VS Code ({numref}`clone1`). Paste the address you copied from GitHub into the top bar and press 'enter' (as shown in {numref}`clone4`). Then select the folder or location on your local machine where you would like the _local repository_ to be stored ({numref}`clone5`).

```{figure} images/clone4.png
---
width: 80%
name: clone4
---
Enter the URL from GitHub and press 'enter'.
```

```{figure} images/clone5.png
---
width: 80%
name: clone5
---
Browse to the location you want to store the _local repository_.
```

As you can see in {numref}`clone5`, we have chosen to put the cloned repository in a directory in the place where we store all code, `code\MUDE`. You don't need to create a new folder for the repository (e.g., `pa-1-3-monadevos` in this example) because the process of cloning a repository will do that automatically. 

`````{admonition} Where to put your local repositories

We strongly encourage you follow these pieces of advice:
1. **Do not** store your local repositories in a location that is backed up using cloud software (e.g., OneDrive, Dropbox, etc). This often interferes with the functioning of git. Instead, we will push to the _remote repositories_ to backup our work.
2. **Do not** store your local repositories in locations with spaces in the file path, especially on Windows. While there are ways to deal with this if it happens, you will save yourself trouble down the line if you avoid using spaces in your folder and file names.
3. **Do** store your local repositories for your project in an organized way. We advise creating a directory for all repositories you have, where each of the sub-directories would be a local git repository. Here is an illustrating of such a structure for your working directories:

```
.
├── Git_repos
|   ├── Repo_1
|   ├── ...
|   ├── Repo_2
│       ├── PA-04.ipynb
│       └── ...
│   └── ...
```
`````

## Creating the clone

At this point you can create the local repository by clicking "Select Repository Destination," which will start the process of downloading the files from GitHub to your computer at the location you chose for local path.

`````{note}
If you were not successful in creating an SSH key and linking it to your GitHub account, this is when you will find out, as a message like this will appear:

```{figure} images/clone6.png
---
width: 80%
name: clone6
---
Error message due to failed SSH setup.
```
% this link needs to be updated
If this happens, go back to the [SSH setup instructions](../../install/git/intro.md)
`````

If you were successful in cloning the repository, you will see something similar to {numref}`clone7` and you can choose to open your _local repository_. Now we are ready to work on the files and preserve the changes by making our first local **commit**!

```{figure} images/clone7.png
---
width: 80%
name: clone7
---
View of the local repository, successfully cloned from the remote on GitLab.
```
