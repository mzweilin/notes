# notes


## Installation on Ubuntu

Update your apt-get and pip (part of the python package in homebrew), then install the virtual environment for better management of python libraries.

```shell
sudo apt-get update
sudo apt-get install python-pip python-dev python-virtualenv

sudo pip install --upgrade pip

pip install --user virtualenvwrapper
```

## Installation on Mac

Update your homebrew and pip (part of the python package in homebrew), then install the virtual environment for better management of python libraries.

```shell

brew update

brew upgrade python
pip install virtualenv
pip install virtualenvwrapper
```

## The common steps

Configure the WORKON folder, write it to `~/.bash_profile`.

```shell

export WORKON_HOME=~/coder/envs
mkdir -p $WORKON_HOME
source /usr/local/bin/virtualenvwrapper.sh
```


Create a new environment for Tensorflow.
```shell

mkvirtualenv tf
```

Install Tensorflow in the virtual environment. (Note the virtualenv indicator before $) Then check the version.


```shell

(tf)$ pip install --upgrade tensorflow
(tf)$ python -c "import tensorflow; print(tensorflow.__version__)"
```

Now you can do anything in the environment without messing up your system-wide environment.

Enter the environment in the future.

```shell
workon tf
```

Leave the environment.
```shell
deactivate
```


