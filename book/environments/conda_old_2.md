## Python environments revisited

```{note}
This page was originally in PA12 README (TSA week; 1 week before Opt week).
```

Until now, we have been able to complete our work in MUDE with a few packages like `numpy` and `scipy` in our `mude` environment, which we create and manage with `conda`. However, as we start to cover more advanced analysis techniques, the need to use special packages increases, because they include, for example, a) specialized numerical techniques that are difficult or tedious to implement in (small) pieces of code, b) numerical schemes are implemented in a way to make computation faster, or c) advanced visualization to help interpret analysis and results.

Unfortunately, each of these packages are themselves require a number of different packages to function properly. To see this, try executing the following command in your Anaconda prompt or terminal (replacing `ENV_NAME` with `mude` for example). You can also try it for `base`.
```
conda env export -n ENV_NAME
```
You should see a long list of packages. Do you remember installing all of them with `conda install` or `pip install`? You shouldn't---but where did they come from? Many of them are packages required by the packages that you _did_ specifically install. These packages are called _dependencies_, and are necessary to make your Python packages function as expected. When you run `conda install numpy`, for example, `conda` checks all of the dependent packages that are needed and makes sure they are also provided in the `environment` that is being created. In reality, this is simply a folder on your computer with all of the `*.py` files stored in it. This _package management_ is what `conda` and `pip` are really doing when you run them with an `install` command. It also checks that it has a suitable _version_ of each dependency; this is why it sometime takes a long time to install a package (imagine you, as `conda install`, going around to all of the other packages stored on your computer and asking _what version of package X do you prefer?_ then trying to figure out how to make everything match with each of them, and doing it for _all_ depedencies!). Unfortunately, this means that as you add more packages to a particular environment, it gets more and more difficult to make sure everything works well together. Luckily, there is a practical solution: create new environments for specific projects to make sure the proper packages can function properly!

### Create environment with specific packages

As you saw during Q1, it is easy to create a new environment with a specific version of Python, for example, with the command: `conda create -n ENV_NAME python=3.11 anaconda`. We can install as many packages as we want when creating the environment by adding them to the end of the list. For example, can you see which packages would be installed by running the following command?

```
conda create -n ENV_NAME python=3.11 numpy scipy
```
Once you require a large number of packages, this can be tedious! Luckily there is a solution: listing the required packages in a text-based file, and then telling `conda` to create the environment based on the contents of the file! 

### Create environment from text-based file

All we need to do to create an environment from a file is to write a list of what we want and then tell `conda` to read it. That's it!

#### List requirements in `*.yml` file

To write our list of requirements, we will use a file with a new (to us) file extension: the `*.yml` file (pronounced "yah-mul"). It is a text-readable file, that stands for "Yet another Markup Language." You don't need to worry about this, except to recognize that this is one of _many_ types of files that use a particular type of text formatting to give a computer specific instructions. It is very similar to the way Markdown formatting works.

Take a look at the contents of the file `environment.yml` in this repository. Can you understand what is being described? For each section (`name` and `dependencies`) you should see that it uses a colon `:` to list the information. This will be processed by `conda` when creating the new environment.

There is another special type of formatting with two colons `::`. This is how we tell `conda` to look on a specific _channel_ for the particular package. Conda channels are the locations where packages are stored; you can think of them as a specific URL web address. This is where the creator of the package can manage and maintain its distribution (e.g., publishing new versions, installation information, etc). Conda packages are downloaded from these URL's, and if you know where a particular package is stored, you can give `conda` explicit instructions. For example, we can see that Gurobi is stored on the `gurobi` channel, because the URL is `https://anaconda.org/gurobi/gurobi` (note that Anaconda is an organization that provides a wide variety of software; the website anaconda.com is used to provide documentation and information about the organization, whereas anaconda.**org** is explicitly used for package distribution).  This is specified in the environment file using the `channel::package` notation. In the `*.yml` file, `gurobi::gurobi` is equivalent to using the command `conda install -c gurobi gurobi` in Anaconda prompt.

In summary, as you can see from reading the file, we will set up an environment specifically for this assignment, PA12, along with a number of dependency packages, two of which are installed from special conda channels.

#### Create environment from `*.yml` file

The command for creating the environment is simple. Do the following:

1. Open Anaconda Prompt (Windows) / your default terminal app (Mac)
2. Navigate to your working directory (where this file and `environment.yml` is located)
3. Execute this command: `conda env create -f environment.yml`
4. Keep reading this assignment as you wait (this may take several minutes)

Do you know why this takes so long? Because we are installing many packages at once! Keep an eye on the terminal window as this process is completed. First `conda` is collecting information about the dependencies, then it will _solve_ the environment; in other words, figure out which version of each package it should use. Once it is ready, it will present the list of packages and peoceed with the "installation" (really just downloading `*.py` files and putting them in a folder on your computer (note that the prompt may ask you to confirm that the installation should proceed, depending on your system settings). 

Once the environment is created, we can activate it, and also check that everything was installed properly. Try `conda env export -n ENV_NAME` to see what was installed by "default." The list is very long, even though we only asked for a few packages!

It is also interesting to try `conda env export --from-history` (make sure you activated it already), which shows the specific packages requested. Do you notice anything in particular when looking at the output? That's right, it's exactly the same as our file `environment.yml`! The only thing extra is that it identifies `default` as the conda channel (since we didn't specify anything else in the `*.yml` file).
