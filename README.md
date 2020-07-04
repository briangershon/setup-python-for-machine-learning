# setup-python

Setting up Python 3.7 for Machine Learning on MacOS.

## Install Python

    brew install python3
    # verify your path is setup correctly to run `/usr/local/bin/python3`.

## Manage Python Virtual Environment

    # create new virtual environment in your projects folder
    python3 -m venv env

    # add "env" to your .gitignore

    # activate environment
    source env/bin/activate

    # optionally upgrade pip
    pip install --upgrade pip

    # install packages, for example:
    pip install pylint tensorflow scikit-learn

    # optionally save all installed python packages into a file
    pip freeze > requirements.txt

    # which can then be loaded via `pip install`
    pip install -r requirements.txt

## Setup Visual Studio Code

- install pylint plugin
- choose "Python: Select Interpreter" command and pick the virtual env one
