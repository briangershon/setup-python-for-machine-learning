# setup-python

Do you have a Python project that needs its own virtual environment?

These are setup instructions for adding a Python 3.7 virtual environment to any project. (MacOS specific)

The advantage of this approach over Anaconda is that your environment is within your project folder and self-contained. Makes it easier to work on across machines.

## Install Python

    Use existing `python3` on MacOS.

    # or install via Homebrew
    brew install python3
    # verify your path is setup correctly to run `/usr/local/bin/python3`.

## Manage Python Virtual Environment

    # create new virtual environment in your projects folder
    # venv is the standard way of creating virtual envs on Python
    python3 -m venv env

    # add "env" to your .gitignore so env is never checked-in

    # activate environment
    source env/bin/activate

    # optionally upgrade pip and setuptools
    pip install --upgrade pip
    pip install setuptools --upgrade

    # install packages, for example:
    pip install pylint tensorflow scikit-learn

    # optionally save all installed python packages into a file
    pip freeze > requirements.txt

    # which can then be loaded via `pip install`
    pip install -r requirements.txt

## Setup Visual Studio Code

- install pylint plugin
- choose "Python: Select Interpreter" command and pick the virtual env one

VS Code then nicely creates a `.vscode/settings.json` in your project which sets the pythonPath for you in your local env.
