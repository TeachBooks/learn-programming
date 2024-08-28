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