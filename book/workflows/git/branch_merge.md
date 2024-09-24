# Branching and merging

## What are branches

So far, we have only been making commits using the `main` or `master` branch, however, in practice, you will work on a separate branch, whose progress you will later merge with `main`.

Commits in git have a graph structure, where every node is a commit and edges represent the transition (flow) between commits. Branches can be thought of as pointers to commits, whereas HEAD points to the current commit that we are at. When you switch between branches, you can think of HEAD as the most recent commit on that branch.

The graph below shows the commit history of a repo with two commits:

![Commit graph of our repository](./images/branch1.png)

The main advantage of version control is that it allows developers to work together in parallel. During projects, you will be working on "feature" branches and separating the work to review and merge it later. A common graphical structure of commits is shown below, where we have developers working on 3 separate branches and merging their work when necessary. This separation offers flexibility, parallelization of work, and offers more control over the development process.

![Commit graph of a sample repository](./images/branch2.png)

## Creating a branch

First, let us check on what branch we are currently at. On GitHub, navigate to your repository and click on the "Branch: main" dropdown to see the list of branches. The branch with a checkmark is your current branch.

![Check existing branches](./images/branch3.png)

Let us create a new branch from `main` on GitHub, which we will call `first-branch`. Click on the "Branch: main" dropdown, type `first-branch` in the text box, and click "Create branch: first-branch".

We can move to the newly created branch by selecting it from the branch dropdown.

![Moving to branch `first-branch`](./images/branch4.png)

Let us modify our `README.md` file again and add a "Getting started" section to it. Navigate to the `README.md` file, click the pencil icon to edit it, and add your content.

We will commit the new changes by filling out the commit message and clicking "Commit changes".

![Committing new changes](./images/branch5.png)

## Merging branches / pull requests

Note that when we switch to `main`, the `README.md` file does not contain the changes we made on the other branch.

Before merging our progress from `first-branch`, it is advisable to merge `main` into it first. This is done because we regard the `main` branch as the "face" of our project. When somebody is looking at our repository, they are likely to check the things on `main` first. Moreover, if there are any bugs from merging, it is better to resolve them on our separate branch. Sometimes it happens that after merging your progress to the `main` branch, the code on the `main` branch is no longer working correctly.

Therefore, we will first go back to our branch `first-branch`. Note that the new file we made is no longer visible. We can merge the `main` branch into `first-branch` by creating a pull request. On GitHub, go to the "Pull requests" tab, click "New pull request", select `main` as the base branch and `first-branch` as the compare branch, and click "Create pull request".

We can now inspect the graph again with the new changes. The progress of the other branch (`main`) has been moved to `first-branch` as seen below.

![New commits graph](./images/branch9.png)

We will now return to `main` and merge `first-branch` into it with another pull request. Follow the same steps as before, but this time select `first-branch` as the compare branch and `main` as the base branch.

![Merging `first-branch` into `main`](./images/branch10.png)

Note that this time we are not prompted to enter a commit message for our merge.

## Deleting branches

Branch `first-branch` has lived its use, so we can delete it as we do not plan on making new changes to it. This will not remove any of the commits made on it. It will only remove the pointer itself. Do this from the pull request page by clicking "Delete branch".

![Deleting a branch](./images/branch12.png)

