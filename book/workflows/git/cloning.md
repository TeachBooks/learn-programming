# Cloning a Repository

This page will show you how to use Source Control in VS Code to **clone** a repository. **Cloning** is the process of duplicating not only the files, but also the record of all changes that have been made to those files in the past (that's what the git software is doing!). Because the history of these files is preserved, even if we make changes to these files in one of the repositories, the git software will provide a way to update the other software some time in the future. This allows multiple people to work on the same files at the same time; or, you as an individual to work on the same files using several different computers (e.g., a work and home laptop).

Creating several clones of a repository allows us to also provide a backup of our files (and their history) in case we lose access to the originals (perhaps your computer breaks, or is stolen). It is a great idea to have a copy of the repository in the cloud, which automatically provides a very reliable file storage location. This is one of the key services that companies like GitLab and GitHub provide. 

In practice we refer to the repository stored on our computer as the **local repository.** This is where we typically spend most of our time working on our code, debugging it and running analysis. It is where you will be spending most of your time working on your MUDE assignments.

% Not sure about the collaboration notes in this part, since i guess they will be using Live Share and then only one person pushes to the remote repo?
The repository on GitHub is our **remote repository.** This can be considered the backup of the files in our repository. When working with multiple people, it can also be considered the most current version of the project. For example, you may be working on improving the plots in your assignment, whereas a colleague is updating the Python script running your model. You will use the _local repository_ to develop your particular task, and the _remote repository_ to collect everyone elses work and deploy it to your local computer (if you need to use it there).

% I just changed GitLab to GitHub
Note that in MUDE, we will use the _remote repositories_ on GitHub to share files with you. After completing this page, you will be able to **clone** the remote repository to your computer with the click of a button. Later pages will show you how to **push** your _local_ changes back to the _remote_, which is how you will submit your assignments for grading.

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

As you can see in {numref}`clone5`, we have chosen to put the cloned repository in the MUDE directory in the place where we store all code, `code\MUDE`. You don't need to create a new folder for the repository (e.g., `pa-1-3-monadevos` in this example) because the process of cloning a repository will do that automatically. 


`````{admonition} Where to put your local repositories

We strongly encourage you follow these pieces of advice:
1. **Do not** store your local repositories in a location that is backed up using cloud software (e.g., OneDrive, Dropbox, etc). This often interferes with the functioning of git. Instead, we will push to the _remote repositories_ to backup our work.
2. **Do not** store your local repositories in locations with spaces in the file path, especially on Windows. While there are ways to deal with this if it happens, you will save yourself trouble down the line if you avoid using spaces in your folder and file names.
3. **Do** store your local repositories for MUDE in an organized way. We advise creating a `MUDE` directory, where each of the sub-directories would be a local git repository. Here is an illustrating of such a structure for your working directories:

```
.
├── MUDE
|   ├── Week_1_1
|   ├── ...
|   ├── Week_1_4
│       ├── PA-04.ipynb
│       └── ...
│   └── ...
```
Adopting this structure will make it very easy for you to submit assignments for MUDE.
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
If this happens, go back to the [SSH setup instructions]()
`````

If you were successful in cloning the repository, you will see something similar to {numref}`clone7` and you can choose to open your _local repository_. Now we are ready to work on the files and preserve the changes by making our first local **commit**!

```{figure} images/clone7.png
---
width: 80%
name: clone7
---
View of the local repository, successfully cloned from the remote on GitLab.
```
