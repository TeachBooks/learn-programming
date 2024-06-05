# Environments

Now we will make sure you have an environment to get started in MUDE. This year we will use Python 3.11, so we are going to make sure that’s installed and ready to go. Other Python packages that are not included in the base installation will be installed in your environment one at a time as we go through our Programming Assignments, to make sure we know exactly what is going on when working with code in MUDE.

The following steps will create an Anaconda environment called mude and install Python 3.11. Even if you already have Python 3.11, it is still good practice to create a dedicated Anaconda environment for each of your major projects (and MUDE is definitely a major project). Please make sure you have upgraded Anaconda before proceeding with these steps:

Open the commmand line interface (see above)—you can also continue in the same session if it is still active
- Execute: `conda create -n mude python=3.11 anaconda` (this may take several minutes)
- Activate: conda activate mude
- Check: you should now see mude displayed somewhere in the prompt between parenthesis, like this: (mude)
One important reminder: throughout the semester you should be using the mude environment every time you use Python, except when instructed otherwise. All you have to do is remember to use the command conda activate mude prior to opening your notebook. The suggested workflow is described in the instructions for Week 1, and you can also find them on the course website here.

Make it a habit of installing packages with the command line interface
We need to make sure the right packages are installed and available, which you should also do from the terminal. The procedure is described on the Packages page (you can also access these instructions directly from the Software page).

Note that we have two “things” called “mude”: an Anaconda environment and a Python package. You will always use an environment when working with a notebook in MUDE (“mude” the first few weeks, but eventually we will create more—the name is arbitrary). The package “mude” is one of many Python packages we will use in the module; you won’t need to use it every time you work on a notebook. You can install the mude package now, or you can wait until you need it for your first programming assignment, it does not matter.

Now that we have our Python environment set up, you’re almost ready to start your first Programming Assignment, but we still have one thing to do: create a suitable place in the file system of your computer to work.

```python
import numpy as np
np.linspace(0,10,11)
```