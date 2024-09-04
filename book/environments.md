(environments)=
# Environments and Environment Managers

This is a brief introduction to _computing environments,_ with a focus on the Python programming language for scientific computing applications.

## What is an environment?

An _environment_ is..._complicated._ Suffice to say it is related to operating system, programming languages and files on your computer, but also related to the hardware (i.e., the processor, etc). For our purposes, it mostly has to do with identifying a specific version of Python as well as the various Python _packages_ (e.g., `numpy`) that are used for a given _project._ Often this concerns specifying _versions_ that are compatible with each other; this is really what `conda` is doing when you ask it to build a new environment, or add a new package (e.g., with `conda install` or `pip install`).

Unfortunately, because computer hardware plays a role in determining compatibility, you may find that while something works perfectly on your own computer, it goes wrong on another. In summary, you can consider an environment as _a specification to define acceptable versions of various code to enable a project (code) to run successfully on your own computer, as well as the computers of others (e.g., fellow students, teachers and cloud-based computers)._

If the concept of an _environment_ facilitates the running of code, an _environment manager_ facilitates the creation, modification, specification, etc, of an _environment_ itself.

The purpose of environments and environment managers is to allow an arbitrary software project to be used on an arbitrary computer, regardless of operating system (although one should note that some OS-specific software is required, for example the environment manager itself). This is illustrated schematically in the following figure.

```{figure} environments/figures/simple.svg
---
width: 80%
name: environments_simple
---
An environment manager ensures that an environment can be set up and used for a particular project on an arbitrary computer. 
```

In a more simple definition, an environment is simply a directory on your computer that contains the source code that has been selected by an environment manager to be compatible with the operating system and hardware on your computer, as well as the source code of the other packages in that same environment. The compatibility between these pieces of software is referred to as _dependency,_ and tools that identify the proper versions of software are called _dependency solvers._ One commonly used example is `conda`.

### How to Create and Environment?

In many applications it is sufficient to determine a specific version of Python (e.g., version 3.12) and a list of the software you would like to use, then as an environment manager to download compatible versions and set up an environment. In a simplified view, this is roughly equivalent to downloading source code and putting it in a directory on your computer.

If one were using the `conda` environment manager, this could be done by listing the desired software in a `environment.yml` file (a simple text-based file) and running the following command:

```
conda env create -f environment.yml
```

Where `-f environment.yml` instructs `conda` which file contains the list of desired software, which contains, for example, Python 3.12 and a number of commonly used Python packages for scientific computing:
```
name: my_environment_name
dependencies:
  - python=3.12
  - numpy
  - scipy
  - pandas
  - matplotlib
```

## Why is an Environment Manager Necessary?

Environments and environment managers make it very easy to share projects between collaborators without the need to make computer-specific versions that are compatible with a wide variety of hardware and operating systems. This is illustrated schematically in the following figure, where multiple environment managers can be used to run projects on different computers. Depending on the requirements of a project or computer, a wide number of environment managers could be considered by the user.

```{figure} environments/figures/complex.svg
---
width: 80%
name: environments_complex
---
There are many types of environment managers that can be selected depending on a particular project, operating system or environment type.
```

## Examples of Environment Managers

One of the most common environment managers for scientific computing is `conda`; this popular command line tool is available many software distributions, for example, Anaconda or Miniconda.

Another popular environment manager is Python itself, via it's own virtual environment module (`venv`). Perhaps unsurprisingly, Python's `venv` is limited to the management of Python packages (primarily via `pip`), unlike `conda`, which can manage software packages and environments that use a wide variety of languages (for example, the R language, or LaTeX and Pandoc software).

### Choosing an Environment Manager

If you are a student, chances are the choice of environment manager has already been made for you. If not, you have a choice to make!

The use of Python virtual environments (`venv`) should be seen as an alternative to `conda` (especially if you installed Anaconda or Miniconda). If you are working primarily with Python packages available on `conda-forge` or PyPI, a `conda` environments will most likely work the same (and can also be easily selected from within VS Code). However, Python virtual environments (`venv`) can be created much more quickly than `conda` environments, and may enable you to manage your Python packages more efficiently in future projects.

However, note that `conda` comes with its own set of advantages, for example, in addition to support beyond Python packages, it has an improved ability to solve for package dependencies, which provides more reliability when distributing more complex software.

## Environment Variables

Modern computers have _environment variables_, which are used to define the behavior of your operating system (which is itself a type of computing environment). These variables are generally not important for most applications covered in this book, as we will focus on computing environments that are more distant from the operating system (for example, a Python environment; not the operating system directly). However, _in particular for users with a Windows operating system,_ it is often needed to change the `PATH` environment variable to make sure various software can be used via a CLI.

Instructions for changing your `PATH` variable on Windows can be found via {ref}`this link <env-vars-windows>`.

Feel free to visit the [wikipedia page](https://en.wikipedia.org/wiki/Environment_variable) for additional explanation or examples.