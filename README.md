# setup-python

Do you have a Python Machine Learning project that needs its own virtual environment?

These are MacOS setup instructions for adding a Python 3.7 virtual environment to any project.

The advantage of this approach over Anaconda is that your environment is within your project folder and self-contained. Makes it easier to work on across machines.

Though if you're just getting started with Python, you may want to go the Anaconda route.

(These virtual environment setup instructions can be used for any project, but focus here is on setting up a Machine Learning environment)

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

    # upgrade pip and setuptools
    pip install --upgrade pip
    pip install setuptools --upgrade

    # install popular ML packages
    pip install pylint tensorflow scikit-learn matplotlib jupyter

    # if you're doing image processing install Pillow (PIL fork)
    brew install libtiff libjpeg webp littlecms
    pip install Pillow

    # optionally save all installed python packages into a file...
    pip freeze > requirements.txt

    # ...which can then be loaded via `pip install`
    pip install -r requirements.txt

## Setup and Run Jupyter Notebooks

Use Jupyter Notebook to edit and run your programs. This supports a nice mix of code, markdown docs, and visual elements like images and plots.

    # install Jupyter
    pip install jupyter

    # start Jupyter server
    jupyter notebook

    # open your `.ipynb` notebook file via Jupyter running in the browser

## Setup Visual Studio Code

If you want to use VS Code editor and run programs (that don't have a visual element):

- install pylint plugin
- choose "Python: Select Interpreter" command and pick the virtual env one

VS Code then nicely creates a `.vscode/settings.json` in your project which sets the pythonPath for you in your local env.
