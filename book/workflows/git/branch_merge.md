# Branching and merging

So far, we have only been making commits using the `main` branch, however, in practice, you will work on a separate branch, whose progress you will later merge with `main`.

Commits in git have a graph structure, where every node is a commit and edges represent the transition (flow) between commits. Branches can be thought of as pointers to commits, whereas HEAD points to the current commit that we are at. When you switch between branches, you can think of HEAD as the most recent commit on that branch.

The graph below shows the commit history of a repo with two commits:

![Commit graph of our repository](https://files.mude.citg.tudelft.nl/branch1.png)

The main advantage of version control is that it allows developers to work together in parallel. During projects, you will be working on "feature" branches and separating the work to review and merge it later. A common graphical structure of commits is shown below, where we have developers working on 3 separate branches and merging their work when necessary. This separation offers flexibility, parallelization of work, and offers more control over the development process.

![Commit graph of a sample repository](https://files.mude.citg.tudelft.nl/branch2.png)

In the commit graph above you see two branches (`Main` and `Dev Branch`). The orange commits `q1` and `q2` were part of a branch but that branch is merged with `main`. The `HEAD` is at `m2`, so if you're looking at the files in repository, you see the stated of all the files after that commit. E.g. the changes from `a1`, `m3` and `q2` (and all others not in front of `m2`) are not visible. So it's not only possible to change branch, but also to go back in time with `Head`!

The `Dev branch` was created from the state of the `Main` branch at `m1` and after two commits `a1` and `a2`, the changes from `m2` have been merged into that branch in commit `a3`.

The orange branch was created from the state of `Main` at `m3`, while after one commit `q1`, the changes from `Dev branch` were included into the orange branch with commit `q2`. After that, it is merged into `Main` at `m5`, effectively merging the `Dev branch` into `Main too`. After that merge, the pointer of the orange branch is deleted, so it's not trivial to go back to the orange branch. However, this can still be done by checking out `Head` to commit `q2`.

## Collaborating with branches

When working together on a branch, it is important to coordinate with your team to avoid conflicts and ensure smooth collaboration. Here are some best practices:

- Keep in touch with your team about who is working on what.
- Frequently pull the latest changes from the remote branch to keep your local branch up to date. This helps in minimizing conflicts.
- Make small, frequent commits with clear messages. This makes it easier to track changes and resolve conflicts.
- Before merging changes, review pull requests carefully. Use GitHub's review features to comment on specific lines and suggest improvements.
- If conflicts arise, communicate with your team to resolve them.