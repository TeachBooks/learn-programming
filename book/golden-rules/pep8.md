(golden-rules-pep8)=
# Style Guide for Python (PEP 8)

PEP stands for Python Enhancement Proposals, which is how the Python community describes new features and guidelines related to the development and (reccommended) use of the programming language. Although there are many [PEPs](https://peps.python.org/), the MUDE Golden Rules are in part inspired by one in particular: [PEP 8 - Style Guide for Python Code](https://peps.python.org/pep-0008/). PEP 8 is important because it directly addresses the readability of Python code and is thus directly aligned with the objectives of our Golden Rules. Unfortunately, PEP 8 can also seem boring, tedious and unimportant to engineers who are learning to use Python. The Golden Rules are created in part to help with this, so for now, we ask that you read carefully the [first](https://peps.python.org/pep-0008/#introduction) and [second](https://peps.python.org/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds) sections of PEP 8 to help understand the general motivation, then scan through PEP 8 to get an idea of the structure. You may want to use the website [pep8.org](https://pep8.org/), which uses text formatting and is (visually) much easier to read. Don't just open the website; you should devote at least 15 minutes reading the text and example code and consider how this might influence the way you write code. You don't need to read every word, but rather focus on the background, justification and examples for the sections that are most relevant to us:  
- Code lay-out: indentation, line length, line breaks, blank lines
- Whitespace
- Comments
- Naming conventions  

After a few minutes of reading, you should have a good idea of the general philosophy and specific ways to change the way you write Python code. Many of these guidelines are incorporated into the Golden Rules, but sometimes PEP 8 will provide more detail or background, and most importantly: example code. Therefore, you should bookmark the website and refer back to it often.

You may have noticed that checking some of the PEP 8 guidelines could be quite tedious, like counting 4 spaces on indentation or checking to make sure there are no spaces at the end of a line. This is just the type of thing that computers are good at! Fortunately there are a number of tools available to autocheck (and even autocorrect) Python code based on some (but not all!) of the reccommendations in PEP 8. The elements of PEP 8 that are most relevant to us are summarized here: 
- Indentation
- Whitespace and blank lines
- Line length and line break location
- Import statements

Compliance with PEP 8 is carried out by the package [`pycodestyle`](https://pycodestyle.pycqa.org/), and you can see a detailed list of what is being checked in your code by looking at the the [list of error codes](https://pycodestyle.pycqa.org/en/latest/intro.html#error-codes). There are a few other PEP 8 guidelines that are not included in the list above or in our Golden Rules (specifically, issues in the statement and runtime groups in `pycodestyle`). If these come up as warnings or errors when reviewing your code with an autochecker you can read more about what the problem is in the PEP 8 documentation.

The next section covers PEP 8 autocheckers, but you should **always remember: only a subset the PEP 8 guidelines can be evaluated by automatic PEP 8 checkers and fixers.** For example, a computer cannot tell you whether or not your variable name is descriptive enough, or consider what variable name length is appropriate for the specific piece of code you are writing---this is something that you must determine on your own or with your team that may be hard at first, but becomes easier with a bit of practice. To convey this perspective, we adapt the quote by Martin Fowler given above:


<div style="text-align: right"><em>Any fool can use </em><code>autopep8</code><em> to comply with PEP 8 guidelines. Good engineers use PEP 8 carefully to write code that humans can understand.</em></div>  
<div style="text-align: right"><em> ― MUDE Golden Rules, adapted from Martin Fowler </em></div> 

## Checking PEP 8 automatically with `autopep8`

Although PEP 8 may look quite complicated and tedious at first glance, automatic PEP 8 formatters exist. The one we recommend you to use is `autopep8`, which can be applied on both `.py` files and `.ipynb` jupyter notebooks. A full explanation about the capabilities of this tool can be found at the [Python Package Index page](https://pypi.org/project/autopep8/).  

*Bonus tip: the Python Package Index, PyPI, is the official website for Python software, where most publicly available packages can be found, and is the default source when you install packages using `pip`.*

### Installation
In order to install `autopep8`, you can simply run the following `pip` command in your terminal:
```bash
pip install autopep8
```

### Usage

You can run the following command to auto-format python files and jupyter notebooks in-place. After the command execution has finished, your files will have been autoformatted. Make sure you replace `<filename>` with the name and extension of the file you wish to auto-format.
```bash
autopep8 --in-place <filename>
```

### Additional Resources

`autopep8` can be added as an extension to JupyterHub, which allows you to interact with the tool through a Jupyter Notebook rather than the terminal. This can be achieved with the help of a `Jupyter Nbextensions Configurator`, which you may need to install first, before setting up `autopep8` as an extension.

Many of the IDEs such as Spyder and PyCharm contain add-ons that can be installed to automate the PEP 8 checks. Rather than providing a long list of installation instructions here, we'd encourage you to already get started with Rule X: using Google and Stack Overflow to help you identify and install a PEP 8 tool that will work for you. If you are using the JupyterHub, you can always copy and paste text into [PEP8 Online](http://pep8online.com/), as done in the first example above.