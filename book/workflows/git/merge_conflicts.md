# Merge conflicts
Merge conflicts arise when people on separate branches modify the same parts of one (or multiple) files. Since Git does not know how to handle that and whose changes to consider, it prompts the user to decide instead.

![Visualisation of a merge conflict](./images/mconflict1.png)

Let us create a merge conflict ourselves:

We will start by making a new branch `conflicting-instructions` on GitHub. We will edit a markdown file, and create a pull request as shown below.

![Creating a pull request](./images/mconflict2.png)

Next, we will return to the `main` branch on GitHub. We will edit the same line of the markdown file with some other text and create another pull request.

Finally, we will attempt to merge the `main` branch into the `conflicting-instructions` branch using the pull request interface on GitHub. This will result in a merge conflict, as seen in the figure below, because we modified the same parts of the file.

![Merge conflict](./images/mconflict5.png)

The changes on the current branch are preceded by `<<<<<<< HEAD`, while the changes from the `main` branch are preceded by `=======` and followed by `>>>>>>> main`. To fix this conflict, we need to open the file in the GitHub editor and resolve the conflict by keeping the desired changes and removing the unnecessary parts. Once done, we can commit the resolved changes directly from the GitHub interface. Note that the current branch is now in a "MERGING" state. We have decided to take the best out of the two branches and merge their changes.

![Completing the merge](./images/mconflict6.png)