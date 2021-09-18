# setup-python-for-machine-learning

These are MacOS setup instructions for adding a Python 3 virtual environment for any project, installing popular Machine Learning packages, and setting up Visual Studio Code editor.

These virtual environment setup instructions can be used for any project, but focus here is on setting up a Machine Learning environment.

I prefer this classic Python virtual environment approach since the environment lives within your project's folder and is self-contained, which makes it easier to work on across machines. You can just clone your project and setup an environment on each machine.

Though if you're just getting started with Python, you may want to go the Anaconda route. Jennifer Walker has some nice [Python setup instructions](https://jenfly.github.io/datajam-python/SETUP).

## Install Python 3 on MacOS

    # Install via Homebrew
    brew install python3
    which python3   # should show `/usr/local/bin/python3`
    python -V       # should show version

## Manage Python Virtual Environment

    # create a folder to hold your project and jump into that folder
    mkdir my-cool-project
    cd my-cool-project

    # create new virtual environment in your projects folder
    # venv is the standard way of creating virtual envs on Python
    python3 -m venv env

    # add "env" to your .gitignore so env is never checked-in
    echo "env" > .gitignore

    # activate environment
    source env/bin/activate

    # upgrade pip and setuptools
    pip install --upgrade pip setuptools wheel

## Setup and Run Jupyter Notebooks

Use Jupyter Notebook to edit and run your programs. This supports a nice mix of code, markdown docs, and visual elements like images and plots.

    # Install Jupyter Notebooks and ipython
    pip install jupyter jupyterlab
    ipython kernel install --user --name=.env

    # start Jupyter notebook or JupyterLab
    jupyter notebook
    jupyter lab

    # open an `.ipynb` notebook file via Jupyter running in the browser

## Install popular Machine Learning packages

    # Install other popular libraries as desired
    pip install numpy pandas matplotlib seaborn plotly
    pip install tensorflow scikit-learn

    # if you're doing image processing install Pillow (PIL fork)
    brew install libtiff libjpeg webp littlecms
    pip install Pillow

## Save installed packages and versions

    # save all installed python packages into a file...
    pip freeze > requirements.txt

    # ...which can then be loaded via `pip install`
    pip install -r requirements.txt

    # to deactive an environment
    deactivate

## Setup Visual Studio Code

If you want to run program directly in Visual Studio Code editor, just install the VS Code Python plugin from Microsoft. It automatically looks for virtual environments in the project's folder.

However if you need to do this manually, choose `View > Command Palette...` then `Python: Select Interpreter` then pick the virtual env one.

For more info, see <https://code.visualstudio.com/docs/python/environments>.
