(cli)=
# Command Line Interface

A _Command Line Interface_ (CLI) is a method of interacting with a computer that involves individual lines of text. These so-called _command lines_ can be entered manually by the user, as well as written in a text-based file and passed on to a computer or application for automatic entry and execution. The alternative to a CLI is a _Graphical User Interface_ (GUI).

```{admonition} Why use a CLI?
:class: tip

A few of the main reasons for using a CLI in engineering work are:
- rudimentary tasks are easily automated and repeated (e.g., copying, moving, renaming files and folders)
- some software does not have a GUI
- a CLI can easily be openend on any modern laptop and can be much faster than using a GUI

For example, once you can use the CLI you will probably find it much easier than using a GUI to navigate to a working directory on your computer, create and activate a computing environment for your project and open and begin working in your chosen IDE.
```

There is a long history of CLI's and many different types; a brief overview and set of examples are provided on this page.

## Definitions and Terms

There are various terms to be aware of, but we will only give a brief explanation here (see [this tutorial](https://www.tutorialspoint.com/difference-between-terminal-console-shell-and-command-line#:~:text=To%20summarize%2C%20a%20terminal%20is,textual%20commands%20into%20the%20shell.) for a more detailed explanation):

- **Terminal**: a piece of hardward for entering data into a computer. How we did it in the "old days" (the [Wikipedia page](https://en.wikipedia.org/wiki/Computer_terminal) has a few examples).
- **Console**: similar to a terminal, but adds hardware, interaction and a few other things (if you want to understand the difference, [try reading this](https://en.wikipedia.org/wiki/Computer_terminal#System_console))
- **Shell**: an application that allows a user to write commands and enter data that can be translated into commands and data that can be executed by the operating system  and hardward on a given computer; in short, this is how your instructions can be interpreted by any computer, regardless of hardward or operating system. A shell generally has two methods for interaction, a _graphical user interface_ (GUI) or a _command line interface_ (CLI).
- **Command Line Interface**: a method of interacting with a computer that involves typing lines of text into an interface; modern CLI's are implemented in shell applications. Visit the [CLI Wikipedia page](https://en.wikipedia.org/wiki/Command-line_interface) for an exhaustive overview of CLI's.

Now that these have been defined, you might realize that most of your life you have probably used a GUI to interact with your computer (remember, your mobile phone is also a computer!). This page is about using the alternative shell interface: a CLI!

You will hear many people and see softawre that use the terms above interachangably (for example, VS Code uses the term "terminal" for all CLI's), but in reality usage of the term _terminal_ or _console_ today generally refers to a _shell_ with a _CLI._ We recommend sticking to the term **command line interface (CLI)**, or simple the **command line** as this is platform independent and captures what we are physically doing with regards to the content in this book: entering and executing commands via a CLI.

## Examples of CLI's

```{warning}
Work in progress!

General overview for different styles (posix, unix, etc) as well as how that translates to different OS's. Then an overview (with tabs?) of the different OS's and how you can get the different styles on each.
```

- unix
- bash
- command prompt (Windows)
- PowerShell (Windows)
- Anaconda Prompt (command prompt and PowerShell versions)

## Basic CLI Skills

% Isabel has tested all the Mac commands on Macbook Pro M1 - 3 September

|  | Mac   | Windows      |
|--|----------|-------------|
|    Present Working Directory  | `pwd`      | `pwd` |
| List content of the present working directory | `ls`        |  `ls`   |
| Change: Change Directory | `cd /path/to/directory` | `cd /path/to/directory`  |
|   Touch: Creates a new file or updates the timestamp  | touch {filename} (`touch my_file.txt`) | touch {filename} (`touch my_file.txt`)|
| Create new directory  | mkdir {directory_name} (`mkdir my_folder`)  | mkdir {directory_name} (`mkdir my_folder`)   |
| Copy: Copies file or directory | cp {source} {target} (`cp my_file.txt my_folder`)| cp {source}  { target} (`cp my_file.txt my_folder`)|
| Moves a file or directory| mv {source} {target} (`mv my_file.txt my_folder`)| mv {source} {target} (`mv my_file.txt my_folder`)|
| Removes: Removes file |  rm {filename} (`rm my_file.txt`) |  rm {filename} (`rm my_file.txt`)|
| Removes: Removes directory|  rmdir {directory_name} (`rmdir my_folder`) |  rmdir {directory_name}  (`rmdir my_folder`) |
| Clear up terminal | `clear` | `clear` |

%below some simple CL to run python from terminal. Perhaps this can go to the python section
**Python**
|  | Mac   | Windows      |
|--|----------|-------------|
|  Varifying and version  | `python3 --version` | `py -3 --version` |
| Opening Python shell | `python3`    |  `py3`   |
| run python files | python3 {py_file_name} `python3 filename.py` | py3 {py_file_name} `py3 filename.py`|
|Open python file in VS Code| code {py_file_name} `code filename.py` | code {py_file_name} `code filename.py` |

Add the code command for opening pythonfile in VS Code. Open pallete `Cmd +Shft + p`  (`<Shell Command: Install 'code' command in PATH> `)

`exit` leaves the CLI


Here is a link for a more detailed command line cheat sheets:

[Windows command line cheat sheet](https://gist.github.com/hofmannsven/8392477) 

[Mac Ternminal command line cheat sheet](https://github.com/0nn0/terminal-mac-cheatsheet)