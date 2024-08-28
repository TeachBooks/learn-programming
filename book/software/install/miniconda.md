(install-miniconda)=
# Miniconda Installation

Delete Anaconda, etc, in advance.


miniconda website
- installer page: https://docs.anaconda.com/miniconda/
- can do exe, but using Windows Command Prompt, this worked very quick and easily
- https://docs.anaconda.com/miniconda/#quick-command-line-install

```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o miniconda.exe
start /wait "" miniconda.exe /S
del miniconda.exe
```

paste (after download and install you may need to hit enter once or twice to complete the last lines, as they may not execute automatically)





```{figure} figures/miniconda_install.png
---
height: 200px
name: miniconda_install
---
Command line installation of Miniconda.
```



check if the installation is findable on your computer by opening the command prompt and typing:
```
conda --version
```
It probably won't work. You need to: 1) check that the software was installed properly, and 2) tell your computer where to find the software

1. default locaiton is in your computer user settings: `C:/Users/<your user name>/miniconda3/`. Inside this folder you should see a number of files, one of which is a subdirectory `./Scripts/` (inside this folder are a number of executables, one of which is `conda.exe`)

Your computer has _environment variables_ which help located key files. YOu will need to edit the `Path` varibale....

screenshots....(3x startomg wotj `emvoronments-...`
 



```{figure} figures/environment_var_search.png
---
height: 50%
name: environment_var_search
---
Search for environment variable settings; note the description _"for your account"_! (Windows only)
```

```{figure} figures/environment_var_miniconda.png
---
width: 50%
name: environment_var_miniconda
---
How to add Miniconda location to Path variable (Windows only).
```

```{figure} figures/environment_var_miniconda_not_system.png
---
height: 50%
name: environment_var_miniconda_not_system
---
Don't set an environment variable for the _system_, only your account (Windows only)!
```

now try executing `conda --version` one more time. It should reply with the version number, for example, `conda 24.7.1` at the time of creating these instructions.

now type `exit` to leave the command prompt. from now on we will use the Anaconda command prompt; this way instructions will be identical regardless of whether you are using Windows or Mac OS!

>open anaconda prompt

```{figure} figures/anaconda_prompt_open_windows.png
---
height: 50%
name: anaconda_prompt_open_windows
---
Open Anaconda Prompt from the Windows menu (Windows only).
```






%```{figure} figures/.png
%---
%height: 200px
%name: 
%---
%
%```