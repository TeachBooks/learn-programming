# Jupyter Lab Workflow

This page assumes you have:
- installed a distribution of Python that includes `conda`, which is available from the command line interface (check this by executing `conda --version`)
- you can navigate to a working directory using a command line interface
- created a `conda` environment for your project (please don't use `base`!)

How to activate a session:
- navigate to your working directory
- activate your environment with `conda activate <my environment>`
- execute  `jupyter lab`
- start working!

## Why this workflow?

Often we are taught to use Jupyter Lab by opening a session from Anaconda Navigator (sometimes the command line), all of which will initialize the session with the root directory as a default directory somewhere in your computer user files. Often you can't access your desired working directory because in Jupyter Lab or Jupyter Notebook it is not possible to navigate to higher-level sub-directories. This workflow forces you to be explicit not only in the working directory for you Jupyter sessions, but also in choosing your computing _environment._

```{note}
Under construction!

Still to come:
- links to relevant pages (e.g., software install, environments)
- formatting to highlight and contrast differences in other workflows...
- ideas? tell Robert!
```