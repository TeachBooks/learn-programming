## File types and git: text versus binary

Version control systems oriented towards software development and programming are typically focused on **text-based files**: files where the contents are viewable on your computer as human-readable text. **Binary files,** on the other hand, are organized and saved with bits (`0`'s and `1`'s) and are not human-readable. Although this may be a simplified description in terms of the way computers store information (you can read more [here](https://en.wikipedia.org/wiki/Binary_file)), it is enough for our purposes to recognize that text-based files are best suited for use with version control system; in other words, your Python code!

* Examples of common text-based file extensions are: `txt`, `md`, `csv`, `ipynb`, `py`, `html`, etc.
* Examples of common binary files are: `pdf`, `ppt`, `xlsx`, `docx`, etc.

```{admonition} Try it!
Try exploring a few files on your computer to confirm wether they are text-based or binary by opening them up in a text editor. You will easily be able to distinguish the difference because one is readable, the other not.

Note that in Windows if you are using Notepad (the default), you will want to select  "Word Wrap" under the "Format" menu to fit the contents of very long lines within the visible width of the window.
```

## Jupyter Notebooks: JSON-format

Jupyter notebooks, `ipynb`, are a special case in the discussion text vs binary. Because while the contents of your Markdown and code cells is saved as text in the file, the output of the code cells is sometimes a binary format. For example, if you create a plot using matplotlib and save the notebook, that plot output will be binary. This unfortunately makes it a little more difficult to use notebooks with version control, but if we are aware of the issue, it is not a problem---we will show you how.

If you tried opening up a notebook in the text editor you would have noticed a structure with curly braces, `{}`. This is [JSON-format](https://en.wikipedia.org/wiki/JSON)] (another file type), which the notebook uses to store information in each cell.

For example, the following two cells in a jupyter notebook:

```{code-cell}
import numpy as np
```

```{code-cell}
np.linspace(0, 1, 10)
```

Looks as follows:

```yaml
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "e7dcf271",
   "metadata": {},
   "outputs": [],
   "source": [
    "import numpy as np"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "24165ce8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0.        , 0.11111111, 0.22222222, 0.33333333, 0.44444444,\n",
       "       0.55555556, 0.66666667, 0.77777778, 0.88888889, 1.        ])"
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.linspace(0, 1, 10)"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "mude-base",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.11"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
```