---
title: "Python Virtual Environments"
permalink: /materials/creating-curating-humanities-data/03-virtual-environments
toc: true
---

*If you already have experience with virtual environments and have a preferred setup, feel free to keep using what you have already*

## What is virtual environment?

This past week we started exploring Python libraries that installed with Python when you set it up on your computer, but that still need to be imported so that we can use it (remember `Pathlib`!). Now we're going to start installing additional libraries that don't come pre-installed with Python. However, before we install these libraries, we need to create a virtual environment. A virtual environment is necessary to keep the libraries we install contained to each project.

The Python documentation explains that: 

> "Python applications will often use packages and modules that don’t come as part of the standard library. Applications will sometimes need a specific version of a library, because the application may require that a particular bug has been fixed or the application may be written using an obsolete version of the library’s interface.

> This means it may not be possible for one Python installation to meet the requirements of every application. If application A needs version 1.0 of a particular module but application B needs version 2.0, then the requirements are in conflict and installing either version 1.0 or 2.0 will leave one application unable to run.

>The solution for this problem is to create a virtual environment, a self-contained directory tree that contains a Python installation for a particular version of Python, plus a number of additional packages." 

You can read more here about [virtual environments](https://docs.python.org/3/library/venv.html#venv-def).

Prior to installing our virtual environment, let's make sure that you have the latest version of `pip`, which stands for "Python Installs Packages." Pip comes built-in to Python, but run this code to ensure you have the right version.

<figure>
    <a href="{{site.baseurl}}/assets/images/install_pip.png">
        <img src="{{site.baseurl}}/assets/images/install_pip.png" alt="install pip" class="image-popup">
    </a>
</figure>


If you get any errors, you can check if you have pip installed by running the following command in your terminal:

```sh
pip3 --version
```

You can also follow the steps here to check if you have pip installed [https://stackoverflow.com/questions/40868345/checking-whether-the-pip-is-installed](https://stackoverflow.com/questions/40868345/checking-whether-the-pip-is-installed).

If you don't have pip installed, you can install it by following the instructions here [https://pip.pypa.io/en/stable/installation/](https://pip.pypa.io/en/stable/installation/).

Now we'll use the built-in Python virtual environment, called `venv`, which you can read more about here [https://docs.python.org/3/library/venv.html](https://docs.python.org/3/library/venv.html). One thing to note is that there are LOTS of different ways to setup your virtual environment (which lots of people have *very* strong feelings about). I like this answer from Stack Overflow for giving an overview of the differing options [https://stackoverflow.com/a/65854168/7437781](https://stackoverflow.com/a/65854168/7437781).

## Virtual Environments in the Terminal

To create our virtual environment, we'll start by opening our terminal and then navigating to the directory where we want to create our virtual environment. I would recommend making the virtual environment in your project director, though another popular choice is to make a directory in your home directory to store all your virtual environments. You can do that with the commands below:

```sh
cd ~  # This will take you to your home directory
mkdir .virtualenvs # This will create a directory called .virtualenvs
cd .virtualenvs # This will take you into the .virtualenvs directory
```

Now that we are in the directory where we want to create our virtual environment (whether that's `is310-coding-assignments` or `.virtualenvs`), we can create it by running the following command:

```sh
python3 -m venv is310-env
```

This doesn't seem to do much, but if you look in your directory you should see a new folder called `is310-env`. This is your virtual environment.

Now you need to activate our virtual environments. We can either do this with the command line and our terminal or via VS Code. Activating the virtual environment just tells your computer to run Python and installed libraries from the virtual environment rather than the global environment. This might seem like unnecessary work, but as we saw in that xkcd comic, a lot of software can create conflicts over time (often called "dependency hell"). This is a way to avoid that.

### Activating Virtual Environments in the Terminal

To activate our virtual environment in the terminal, we need to use a command called called `source` and after that we need to specify the path to the `activate` file in our virtual environment. The path to the `activate` file is `[LOCATION - OPTIONAL]/[NAME OF VIRTUAL ENVIRONMENT]/bin/activate`. If you aren't in the same directory as your virtual environment, you'll have to specify the exact location of the virtual environment. If you are in the same directory as your virtual environment, you can just run the following command if you're on a Linux/Unix/MacOS system:

```sh
source is310-env/bin/activate
```

Or if you are using a Windows system, you can run the following command for Command Prompt:

```sh
is310-env\Scripts\activate
```

Or for PowerShell:

```sh
.\is310-env\Scripts\Activate.ps1
```

In this example, `is310-env` is the name of the virtual environment.

The `source` command tells the terminal to run the commands in the `activate` file. This will change the prompt in your terminal to show the name of your virtual environment. This is how you know that your virtual environment is activated.


### Activating Virtual Environments in VS Code

<div class="notice--info">⚡️ This information has been adapted from <a href="https://code.visualstudio.com/docs/python/environments">https://code.visualstudio.com/docs/python/environments</a></div>

If you're using VS Code, you can create a virtual environment by opening the Command Palette (⇧⌘P), searching for the Python: Create Environment command, and selecting it. You'll see two options: `Venv` or `Conda`. You can choose either, but I would recommend using `Venv`.

<figure>
    <a href="https://code.visualstudio.com/assets/docs/python/environments/create_environment_dropdown.png">
        <img src="https://code.visualstudio.com/assets/docs/python/environments/create_environment_dropdown.png" alt="Create Environment Dropdown" class="image-popup">
    </a>
</figure>

Once you select `Venv`, you'll be prompted to select the Python interpreter you want to use. You can choose the one that comes with Python, or you can select a different one if you have multiple versions of Python installed on your computer.

<figure>
    <a href="https://code.visualstudio.com/assets/docs/python/environments/create_environment_name.png">
        <img src="https://code.visualstudio.com/assets/docs/python/environments/create_environment_name.png" alt="Create Environment Name" class="image-popup">
    </a>
</figure>

After you've selected the Python interpreter, it will automatically create in your project directory and name it `.venv`. You can right click on the `.venv` folder to rename it to something more descriptive.  For example, if you're working on a project called `is310-coding-assignments`, you could name your virtual environment `is310-env`.

Now to activate your virtual environment, you simply select `New Terminal` under the `Terminal` menu and it will automatically activate your virtual environment. You can tell that it's activated because the name of your virtual environment will appear in the terminal prompt.

## Installing Libraries in Virtual Environments

Now try installing the Python package `Beautiful Soup` by running the following command:

```sh
pip3 install beautifulsoup4
```

You can test if it worked by starting your python interpreter with the `python3` command and running the following code:

```shell
import bs4
bs4.__version__
```

Which should show the version of Beautiful Soup you have installed. We'll be discussing this particular library in our next lesson, but just know that all future libraries you install will be installed in your virtual environment.

And that's it! You've created your first virtual environment and installed a library in it. You can deactivate your virtual environment by running the following command:

```sh
deactivate
```

You can also close your terminal and open a new one to deactivate your virtual environment.

## Additional Resources

- [Python Virtual Environments](https://docs.python.org/3/library/venv.html)
- [Python Virtual Environments: A Primer](https://realpython.com/python-virtual-environments-a-primer/)


