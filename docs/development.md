# Setting up development environment (Unix-like OS)

To setup a development environment, recommended steps are:

1. clone the source code
2. create Python virtual environment
3. start developing :-)

Python 3 is required.

This mini-howto is unix specific, please make necessary changes before
running on windows.

## Prerequisites

On Linux, if you use your distribution packages of Python, make sure you
have venv library (part of standard Python library since 3.3), which can be
distributed separately.  For example on Debian:

```bash
apt-get install python3-venv
```

## Develop

```bash
# clone the project
git clone https://github.com/gabfl/vault && cd vault

# create virtual environment
venv=./var/env && mkdir -p $venv  # suggested directory, choose anything to your liking
python3 -m venv $venv             # make sure you use Python 3
. $venv/bin/activate              # activate the environment

# install necessary packages
pip install wheel pylint pep8 nose ipython # those one are handy for any
Python development
pip install -e .                           # those are vault requirements

# run the program
python -m src
```
