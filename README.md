# C4V-Py

## Installation

Use pip to install the package:
```
pip install c4v-py
```

## Development

The following tools are used in this project:
- [Poetry](https://python-poetry.org/) is used as package manager.
- [Nox](https://nox.thea.codes/) is used as automation tool, mainly for testing.
- [Black](https://black.readthedocs.io/) is the mandatory formatter tool.
- [PyEnv](https://github.com/pyenv/pyenv/wiki) is recommended as a tool to handle multiple python versions in your machine.

The library is intended to be compatible with python ~3.6.9, ~3.7.4 and ~3.8.2. But the primary version to support is ~3.8.2.

The general structure of the project is trying to follow the recommendations
in [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/).
The main difference lies in the source code itself which is not constraint to data science code.

### Setting up your machine to contribute
1. Install pyenv and select a version, ie: 3.8.3.  Once installed run `pyenv install 3.8.3`
2. Install poetry in your system
3. Clone this repo in a desired location `git clone https://github.com/code-for-venezuela/c4v-py.git`
4. Navigate to the folder `cd c4v-py`
5. Make sure your poetry picks up the right version of python by running `pyenv local 3.8.3`, if 3.8.3 is your right version.
6. Since our toml file is already created, we need to get all dependencies by running `poetry install`. This step might take a few minutes to complete.
7. Install nox
8. From `c4v-py` directory, on your terminal, run the command `nox -s tests` to make sure all the tests run.

If you were able to follow every step with no error, you are ready to start contributing.

## Pending

- [ ] Change the authors field in pyproject.toml
- [ ] Change the repository field in pyproject.toml 
- [ ] Move the content below to a place near to the data in the data folder or use the reference folder.
Check [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) for details.
- [ ] Understand what is in the following folders and decide what to do with them.
    - [ ] brat-v1.3_Crunchy_Frog
    - [ ] creating_models
    - [X] data/data_to_annotate
    - [ ] data_analysis
- [ ] Set symbolic links between `brat-v1.3_Crunchy_Frog/data` and `data/data_to_annotate`.  `data_sampler` extracts to `data/data_to_annotate`.  Files placed here are read by Brat.
    - [ ] Download Brat - `wget https://brat.nlplab.org/index.html`
    - [ ] untar brat - `tar -xzvf brat-v1.3_Crunchy_Frog.tar.gz`
    - [ ] install brat - `cd brat-v1.3_Crunchy_Frog && ./install.sh`
    - [ ] replace default annotation conf for current configuration - `wget https://raw.githubusercontent.com/dieko95/c4v-py/master/brat-v1.3_Crunchy_Frog/annotation.conf -O annotation.conf`
    - [ ] replace default config.py for current configuration - `wget https://raw.githubusercontent.com/dieko95/c4v-py/master/brat-v1.3_Crunchy_Frog/config.py -O config.py`
