# Environments

Once installed, we will check to make sure you are ready to use Python. Anaconda provides environments, like small virtual mini-computers inside your real computer, and inside each of those environments you have Python (and a lot of Python packages, probably). Let’s try it:

1. Open a command line interface on your computer:
  - Windows users: this will be the anaconda or conda prompt (search for it in the Start menu at the bottom left of your screen)
  - Mac users: use the “terminal” application
2. Once the command line interface is open, type then execute (hit return) the following: `python --version`
3. You should be running at least Python 3.11. If not, don’t worry, we will try to fix it below (but first make sure you have updated Anaconda as described above)
4. Which environment are you in? The name is between parenthesis at the bottom of your Anaconda Prompt: by default, this should be `(base)`.
5. How many other environments do you have? Execute `conda env list` to see a complete list.
6. Do you see the `*` in the list of environments? That is indicating your current active environment. Unless you have changed something, it should be `base`. And if you just installed Anaconda or Miniconda for the first time, this will be your only environment!

Now we will make sure you have an environment to get started in MUDE. This year we will use Python 3.11, so we are going to make sure that’s installed and ready to go. Other Python packages that are not included in the base installation will be installed in your environment one at a time as we go through our Programming Assignments, to make sure we know exactly what is going on when working with code in MUDE.

The following steps will create an Anaconda environment called `mude` and install Python 3.11. Even if you already have Python 3.11, it is still good practice to create a dedicated Anaconda environment for each of your major projects (and MUDE is definitely a major project).

1. Open the commmand line interface (see above)—you can also continue in the same session if it is still active
2. Execute: `conda create -n mude python=3.11 anaconda` (this may take several minutes)
3. Activate: `conda activate mude`
4. Check: you should now see `mude` displayed somewhere in the prompt between parenthesis, like this: `(mude)`
One important reminder: throughout the semester you should be using the `mude` environment every time you use Python, except when instructed otherwise. All you have to do is remember to use the command `conda activate mude` prior to opening your notebook. The suggested workflow is described in the instructions for Week 1, and you can also find them on the course website here.