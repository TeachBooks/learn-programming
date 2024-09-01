(vsc)=
# Visual Studio Code (VSC)

Visual Studio Code (VSC) is and _Integrated Development Environment_ (IDE): a software that helps users program more effectively, as it combines different workflows in one place. For our purpose VSC is very useful because allows us to do things in one place, for example:
- manage files and sub-directories within our working directory
- execute Python code (and any other programming language!), including Jupyter notebooks
- manage Python environments
- use Git and version control
- many other things, especially with Extensions!

Although Jupyter Lab and Jupyter Notebook are also IDE's, they don't provide as many features as VSC, or maintenance and improvement of tools is slower because the Jupyter development community is smaller. The availability of extensions in VSC, in particular, is exceptional. 

## VSC Installation

The primary steps are:
- download the installer from [code.visualstudio.com/download](https://code.visualstudio.com/download)
- install on your computer (default settings are fine)
- get familiar with the interface
- install a few useful Extensions (see {ref}`overview page <extensions-vsc>`)
- use it!

## Adding Extensions

Extensions are managed in the left-side toolbar of VSC (click the icon with 4 blocks). It is generally very intuitive to search through the avalable extensions and install them. A general overview with descriptions of commonly used extensions and tips for managing is provided on the `{ref}Extensions page <extensions-vsc>`. If your primary goal is to use VSC with Python and Jupyter software (e.g., Jupyter Lab, Jupter Notebook or Jupyter Book), we recommend you start with two extensions:
- Python (Extension ID: `ms-python.python`)
- Jupyter (Extension ID: `ms-toolsai.jupyter`)

```{tip}
Note that if you are using the Jupyter extension it is good to include `ipykernel` in your Python environments (but VSC will add this automatically for you if you don't - isn't VSC great?!).
```

## A Useful Tip (Command Palette)

VSC is very easy to customize, and you can spend hours optimizing it for your own personal use and projects. We recommend skipping this for now if you are just getting started. However, it is useful to know about the _Command Palette,_ which governs all functionality of VSC, and can be accessed with `CTRL+SHIFT+P`. _This is the single most important VSC command to remember._

## Using a CLI (a VSC "Terminal")

VSC refers to a Command Line Interface (CLI) with the term "Terminal."

You can open a new Terminal with the menu bar at the top. Once a Terminal is active you can open additional Terminal instances, chossing amongst the various CLI's available on your computer. It can be useful to have more than one CLI open at a time and keep them collected together with your project files!

To have a specific CLI open by default when you open a Terminal in VSC, open the Command Palette (`CTRL+SHIFT+P`), select the option `Terminal: Select Defaulty Profile` and select your preferred CLI from the list.

## Activating a Python Environment

The easiest way to do this is to make sure you have the Python extension installed, then try to run the cells of a notebook or execute a `*.py` file (look for the play button icon once you have either of these file types open). Upon clicking the run button you will see that VSC asks you to choose a Python kernel. You can choose a Python virtual environment (`venv`) if you have one, but you should also be able to see your `conda` environments as well.

Remember that if you need to install more packages, you should open a CLI (this is called a "terminal" in VSC) and use `pip`, which you can do directly from VSC.

## Using Git and Version Control (Optional)

Git (a version control software) is very nicely integrated within VSC. If you are working on code and text-based projects, the use of Git is strongly encouraged (although if you are a student, we recommend you wait until it is introduced in class before proceding further).

Additional information is provided on the {ref}`Git page for VSC <vsc-git>`.