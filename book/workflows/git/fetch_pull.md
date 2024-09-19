# Fetch and Pull from the Remote Repository

At this point we have seen how to clone a remote repository to make a local repository, make commits to either of them directly, and push from local to remote. There is one more critical skill for being able to use git in MUDE: getting changes on remote back to our local repository. We accomplish this in two stages: **fetching** and **pulling**.

Both of these terms refer to an action we take to get information about updates (e.g., new commits) that have been made to the remote repository (origin). We execute the commands from the local repository.

## Definitions

**Fetch** is when we ask git to connect to the remote repository and see what changes have been made. **Pull** is when we actually implement those changes locally and change the contents of the file on our computer.

**Why two steps?**

Sometimes we are making changes to the files on our computer and we just want to see if something new has happened. **Fetch** allows us to check this without making conflicting changes to our local machine.

```{note}
It is good practice to make it a habit of fetching first, then pulling once you are sure there are no conflicts.
```

## Fetch-pull from remote

Let's first make a commit to the remote repository as explained in [the first chapter](commits_remote.md)

Now we can include the commit in our local repository that we have open in VS Code. We can either right-click on the three dots next to "SOURCE CONTROL" and "Fetch" ({numref}`fetch_pull1_VSC`) or click on the little "Fetch" icon next to "SOURCE CONTROL GRAPH".

```{figure} images/fetch_pull1.png
---
width: 40%
name: fetch_pull1_VSC
---
How to fetch from remote, option 1.
```
```{figure} images/fetch_pull2.png
---
width: 40%
name: fetch_pull2_VSC
---
How to fetch from remote, option 2.
```

As you can see in ({numref}`fetch_pull3_VSC`), under the Source Control Graph we can now see the new commits that have been made (purple) and we can click on one to see the specific changes that have been made. We can now pull all the new commits to our local repository by clicking "Sync Changes".

```{figure} images/fetch_pull3.png
---
width: 100%
name: fetch_pull3_VSC
---
Check the new changes and pull the commits to the local repository
```

## Confirm local changes

Once the commit has been pulled to the local repository, we can open up the file to confirm.
{numref}`fetch_pull4_VSC`

```{figure} images/fetch_pull4_VSC.png
---
width: 100%
name: fetch_pull3
---
Local file `README.md` has the changes made with the Web IDE commit on the remote repository.
```

It's the commits we made on the remote repository!