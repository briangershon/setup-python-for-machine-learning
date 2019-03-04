setup-python
===========

Setting up Python for Machine Learning.

Install Python
--------------

Install Anaconda or Miniconda to create Python 3.7+ virtual envs and download machine learning libraries.

Visit https://docs.anaconda.com/anaconda/install

Manage Python Virtual Environment
---------------------------------

    # create new virtual environment
    conda create -n my-project python=3.7

    # activate your project's virtual environment
    conda activate my-project

    # double-check everything is working and you have correct version
    python --version

    # which Python packages are installed?
    conda list

    # install a package, for example:
    conda install scikit-learn

    # what virtual environments do I already have?
    conda info --envs
