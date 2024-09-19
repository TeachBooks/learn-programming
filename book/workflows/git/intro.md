# Workflow git

There are many methods for using git and GitLab/GitHub: This workflow will focus on using Source Control integrated in VS Code with GitHub.

This Chapter assumes you have already installed the git software, as described [here](../../install/git/intro.md).

In practice we refer to the repository stored on our computer as the **local repository.** This is where we typically spend most of our time working on our code, debugging it and running analysis.

The repository on GitHub is our **remote repository.** This can be considered the backup of the files in our repository. When working with multiple people, it can also be considered the most current version of the project. For example, you may be working on improving some plot, whereas a colleague is updating the Python script running your model. You will use the _local repository_ to develop your particular task, and the _remote repository_ to collect everyone elses work and deploy it to your local computer (if you need to use it there). In education, the remote repositories are used to share your work with your teacher.

The sections within this chapter cover the following concepts:
1. Making commits to the remote repository using the online GitHub IDE
2. Cloning a remote repository from your TU Delft GitHub
3. Making commits to the local repository
4. Pushing your commits back to the remote repository
5. Fetching and pulling commits from the remote repository to your local repository

```{note}
The examples in this page will be illustrated using an arbitrary public repository set up by a MUDE TA on GitHub called [sandbox-public](https://github.com/monadevos/sandbox-public/). You can follow along by [creating your own repository in your GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository).

If you create your own repository, keep the box checked to initialize with a `README.md` file, which will look identical to that in the examples in the following pages.
```