(install-miniconda)=
# Miniconda Installation

Miniconda is smaller version of Anaconda that is very quick and easy to install. Like Anaoncda, it contains the essential tools to start working with Python: `conda`, Python and a few related packages. You can read more about it on the [Miniconda website](https://docs.anaconda.com/miniconda/).

The screenshots in these instructions were made using the Command Prompt on a Windows Operating System (screenshots are from Windows 10). Where needed, instructions and notes for Mac users are provided in addition.

```{tip}
Unless you have installed Anaconda or Miniconda recently (e.g., within the last 2 years), we recommend you completely remove older versions of these softawre distributions from your computer and start from scratch. While it is possible to upgrade them, in our experience it is usually faster and less problematic to simply reinstall.
```

## Download and Installation

As described on the [Miniconda website installer page](https://docs.anaconda.com/miniconda/#quick-command-line-install), Miniconda can be installed by running the following in the Windows Command Prompt:

% Robert tested Aug-24 Windows 10; this worked very quick and easily

````{tab} Windows

As described on the Miniconda site, _these three commands quickly and quietly download the latest 64-bit Windows installer, rename it to a shorter file name, silently install, and then delete the installer._

```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o miniconda.exe
start /wait "" miniconda.exe /S
del miniconda.exe
```
````

````{tab} Mac
As described on the Miniconda site, _these four commands download the latest M1 version of the MacOS installer, rename it to a shorter file name, silently install, and then delete the installer._

```
mkdir -p ~/miniconda3
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh -o ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```
````

```{admonition} Tip for Windows Users
:class: tip
Note that depending on your Windows settings `CTRL+V` does not always work; you may need to use the menu bar of the terminal window or right-click and select paste. In addition, the paste feature typically works one line at a time, therefore after the first line is executed (download) you may need to hit enter once or twice to complete the last lines, as they may not execute automatically.
```

```{figure} figures/miniconda_install.png
---
height: 200px
name: miniconda_install
---
Command line installation of Miniconda (Windows).
```

## Check Whether Installation Was Successful

The easiest way to check if everything worked properly is to make sure that the `conda` command line tool can be found and executed on your system, which can be done by opening the command prompt and typing `conda --version` (note the two dashes, `--`, not one, `-`!). Depending on your operating system and CLI, you should get the following:

```none
C:\Users\rlanzafame>conda --version
conda 23.11.0
```

Usually this works smoothly on a computer with Mac OS, but additional steps are needed for Windows users.

````{admonition} Completing the Installation for Windows OS
:class: tip, dropdown

On a Windows machine running `conda --version` probably won't work the first time because the Windows Command Prompt doesn't know where to find the executable file `conda.exe`. You can resolve this in two simple steps:

1. Find the location of `conda.exe` on your computer.

The executable file `conda.exe` is what allows you to run the command `conda` from a CLI. The default location of this file is in your computer user settings: `C:/Users/<your user name>/miniconda3/`. Inside this folder you should see a number of files, one of which is a subdirectory `./Scripts/`; inside this folder are a number of executables, one of which is `conda.exe`. Therefore, the complete path to `conda` is usually this:

```none
C:\Users\<your user name>\miniconda3\Scripts\conda.exe
```

```{tip}
Can't find the file and folders described above?

Check out the {ref}`Hidden Files and Folders page<hidden>`!
```

2. Tell your computer how to find `conda.exe`

This involves adding the file location found in the previous step to the `PATH` environment variable.

If you don't know how to do this, read the {ref}`environment variable instructions for Windows OS <env-vars-windows>`.
````

## Using Anaconda Prompt

Now that Miniconda is installed on your system, from now on we will use the Anaconda Prompt; this way instructions will be identical regardless of whether you are using Windows or Mac OS!

````{tab} Windows OS

Open the Windows tool bar and begin typing "Anaconda". You should soon see two options appear: "Anaconda Prompt" and "Anaconda PowerShell Prompt." There two versions are based on the two primary CLI's on Windows: Command Prompt and PowerShell. Unless you are an experienced PowerShell user, we recommend using the Command Prompt version: Anaconda Prompt (see figure below):
```{figure} figures/anaconda_prompt_open_windows.png
---
width: 60%
name: anaconda_prompt_open_windows
---
Open Anaconda Prompt from the Windows menu.
```
````
````{tab} Mac OS
```{warning}
Work in progress!
```
````






%```{figure} figures/.png
%---
%height: 200px
%name: 
%---
%
%```