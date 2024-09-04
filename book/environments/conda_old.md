# Environments

Once installed Anaconda, we will check to make sure you are ready to use Python. Anaconda provides environments, like small virtual mini-computers inside your real computer, and inside each of those environments you might have Python (and a lot of Python packages, probably). Let’s try it:

1. Open a command line interface on your computer:
    - Windows users: this will be the anaconda or conda prompt (search for it in the Start menu at the bottom left of your screen)
    - Mac users: use the “terminal” application
2. Once the command line interface is open, type then execute (hit return) the following: `python --version`
3. You should be have a somewhat [recent version of Python](https://www.python.org/doc/versions/). If not, don’t worry, we will try to fix it later on
4. Which environment are you in? The name is between parenthesis at the bottom of your Anaconda Prompt: by default, this should be `(base)`.
5. How many other environments do you have? Execute `conda env list` to see a complete list.
6. Do you see the `*` in the list of environments? That is indicating your current active environment. Unless you have changed something, it should be `base`. And if you just installed Anaconda or Miniconda for the first time, this will be your only environment!

Now we will make sure you have an environment to get started. We'll just make sure `pip` is included in this environment so we can use that to install more stuff later on.

The following steps will create an Anaconda environment:

1. Open the command line interface (see above)—you can also continue in the same session if it is still active
2. Execute: `conda create -n myenv pip` (this may take several minutes)
3. Activate: `conda activate myenv`
4. Check: you should now see `myenv` displayed somewhere in the prompt between parenthesis, like this: `(myenv)`
One important reminder: throughout your project, you should be using the `myenv` environment every time. All you have to do is remember to use the command `conda activate myenv` prior to opening your preferred code editor, or select the `myenv` environment from without your code editor.