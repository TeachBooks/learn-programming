(hidden)=
# Hidden Files

By default some of the folders (directories) and files are hidden on your computer to protect you against making changes that causes problems. You will need to see some of these files and folders to properly set up and use the softare described in this book.

## Change Settings via a GUI

### Windows OS

Settings for hidden files and folders can be found directly via the Windows File Explorer. First find the "options" or "settings" configuration window (sometimes pressing the `ALT` button toggles the menubar on and off): 

```{figure} figures/hidden_windows_1.png
---
width: 60%
name: hidden_windows_1
---
Find the options window for your directory (Windows).
```

Then navigate to the proper location in the "View" tab of the Folder Options window:

```{figure} figures/hidden_windows_2.png
---
width: 60%
name: hidden_windows_2
---
Show hidden files and folders for your directory (Windows).
```

### Mac OS

```{warning}
Work in progress!
```

## Use the Command Line Interface (CLI)


If you would like to view hidden files and folders via the command line, this is illustrated with the simple commands here (review the {ref}`CLI page <cli>` for an overview of the different systems):

````{tab} Unix-type CLI
The option `a` lists all files (including hidden ones) and the `l` presents the output in a nicely formatted list (one item per row):
```bash
ls -la
```
````
````{tab} Command Prompt (Windows)
The command:
```
dir /a:h
```
will list hidden files in the current directory, whereas the following will list hidden directories:
```
dir /a:d
```
````
````{tab} PowerShell (Windows)
There are two options to try:
```powershell
Get-ChildItem -Force
dir -Force
```
In case you run into trouble here, try [this Stack Exchange answer](https://stackoverflow.com/questions/73207344/whats-the-cmd-line-equivalent-of-ls-a-in-powershell-on-windows-vscode).
````