# Merge conflicts
Merge conflicts arise when people on separate branches modify the same parts of one (or multiple) files. Since Git does not know how to handle that and whose changes to consider, it prompts the user to decide instead.

![Visualisation of a merge conflict](https://files.mude.citg.tudelft.nl/mconflict1.png)

Git and GitHub assist you in solving these conflicts, as seen in the figure below:

![Merge conflict](https://files.mude.citg.tudelft.nl/mconflict3.png)

In this situatie, it is attempted to merge main in a conflicting branch. The conflicting lines on the main branches are preceded by `<<<<<<< main`, while the changes from the conflicted `main` branch are preceded by `=======` and followed by `>>>>>>> conflicting-instructions`. To fix this conflict, we need to open the file in an editor (either on GitHub or locally on your computer) and resolve the conflict by keeping the desired changes and removing the unnecessary parts. Once done, we can commit the resolved changes . Note that the current branch is now in a "MERGING" state. We have decided to take the best out of the two branches and merge their changes.

## Why Merge into the conflicting branch first?

Merging into the conflicting branch first allows you to resolve conflicts in a controlled environment. Here are some reasons why this approach is beneficial:

- By resolving conflicts in the feature or conflicting branch, you isolate the changes and ensure that the main branch remains stable and conflict-free.
- In case of coding, you can thoroughly test the merged changes in the conflicting branch before integrating them into the main branch, reducing the risk of introducing bugs.
- Keeping the main branch clean and conflict-free simplifies the integration process and makes it easier for other team members to continue their work without interruptions.

## Why notebooks causes conflicts all the time

Yeah, this is really annoying. The JSON structure of a notebook causes the issue, as explained [here](../../version_control/notebooks.ipynb).