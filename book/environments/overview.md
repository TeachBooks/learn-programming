(environments)=
# Computing Environments

```{warning}
Work in progress!
```

This is the landing page for environments.

_Note: the use of Python virtual environments (`venv`) to manage an environment should be seen as an alternative to `conda` (especially if you installed Anaconda or Miniconda). If you are working primarily with Python packages available on `conda-forge` or PyPI, a `conda` environments will most likely work the same (and can also be easily selected from within VS Code). However, Python virtual environments (`venv`) can be created much more quickly than `conda` environments, and may enable you to manage your Python packages more efficiently in future projects._ 

## What is an environment?

An _environment_ is..._complicated._ Suffice to say it is related to operating system, programming languages and files on your computer, but also related to the hardware (i.e., the processor, etc). For our purposes, it mostly has to do with identifying a specific version of Python as well as the various Python _packages_ (e.g., `numpy`) that are used for a given _project._ Often this concerns specifying _versions_ that are compatible with each other; this is really what Anaconda is doing when you ask it to build a new environment, or add a new package (e.g., with `conda install` or `pip install`). Unfortunately, because computer hardware plays a role in determining compatibility, you may find that while something works perfectly on your own computer, it goes wrong on another. In summary, you can consider an environment as _a specification to define acceptable versions of various Python code to enable a project (code) to run successfully on your own computer, as well as the computers of others (e.g., fellow students, teachers and cloud-based computers)._

In this course we will use Python 3.11 and specify our environment using a `requirements.txt` file and manage the installation with two standard packages of Python: virtual environments (`venv`) and `pip`.

## Environment Variables

Modern computers have _environment variables_, which are used to define the behavior of your operating system. These are generally not important for most applications covered in this book, as we will focus on computing environments that are more distant from the operating system (for example, a Python environment; not the operating system directly). However, _in particlar for users with a Windows operating system,_ it is often needed to change the `PATH` enviornment variable to make sure various software can be used via a CLI.

Instructions for changing your `PATH` variable on Windows can be found via {ref}`this link <env-vars-windows>`.

Feel free to visit the [wikipedia page](https://en.wikipedia.org/wiki/Environment_variable) for additional explanation or examples.