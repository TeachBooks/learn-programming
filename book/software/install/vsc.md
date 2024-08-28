(vsc)=
# Visual Studio Code (VSC)

Visual Studio Code (VSC) is and _Integrated Development Environment_ (IDE): a software that helps users program more effectively, as it combines different workflows in one place. For our purpose VS Code is very useful because allows us to:
- manage files and sub-directories within our working directory
- execute Python code (and any other programming language!), including Jupyter notebooks
- manage Python environments
- use Git and version control
- many other things, especially with Extensions!

Although Jupyter Lab and Jupyter Notebook are also IDE's, they don't provide as many features as VS Code. The availability of extensions, in particular, is exceptional. 

## Installation

The primary steps are:
- download the installer from [code.visualstudio.com/download](https://code.visualstudio.com/download)
- get familiar with the interface
- install a few useful Extensions
- use it!

### Extensions

Select the "Extensions" box on the left side of the application (the symbol is four boxes), then search for and install the following (entering the ID in the search box turns up the right result):
- Python (Extension ID: `ms-python.python`)
- Jupyter (Extension ID: `ms-toolsai.jupyter`)
- GitHub Pull Requests (Extension ID: `GitHub.vscode-pull-request-github`)

### Using Git and Version Control

_Note that you can still use GitHub Desktop in parallel with VS Code without issue. The choice comes down to personal preference; although the user interface is different, both tools manage Git and your remote repositories in a similarly._

We will use the HTTPS protocol for cloning repositories, since VS Code allows you to authenticate yourself by logging in to your GitHub account via the application (this avoids setting up SSH).

It is very easy to clone a repository and start working on a project:
- Copy the HTTPS clone link from the repository on github.com
- Open a new window (File >>> New Window)
- Under the "Start" menu, select "Clone Git Repository"
- Paste the link, then choose the location where you would like to store the repository (hint: in your `.../HOS/` directory!)

You should have already installed the extension GitHub Pull Requests, which will allow you to log in to GitHub. After this you will be able to push back to the remote repository (github.com) using the "Source Control" tab on the left of the application.

### Activating a Python Environment

The easiest way to do this is to make sure you have the Python extension installed, then try to run the cells of a notebook. You will see that VS Code asks you to choose a Python kernel. You can choose a Python virtual environment (`venv`) if you have one, but you should also be able to see your `conda` environments as well.

Remember that if you need to install more packages, you should open a terminal and use `pip`, which you can do directly from VS Code.