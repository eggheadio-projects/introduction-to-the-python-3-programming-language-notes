# [Manage Dependencies with Python Virtual Environments](https://egghead.io/lessons/python-manage-dependencies-with-python-virtual-environments)

## What are Virtual Envrionments?

A virtual environment is a tool used in Python to keep project dependencies in separate places.

## Installing and Setting Up Your Virtual Environment

Follow these steps to intall your virtual environment, run this command

`pip install virtualenv`

Follow these steps when you want to execute your virtual environment in a project.

### 1. Create a directory for your project

### 2. Change into that directory

### 3. Create the virtual environment with the virtual env command along with a name for your virtual environment

`virtualenv py3 -p /usr/local/bin/python3`


Typing `/usr/local/bin/python3` specifies that you want to use Python 3.

### 4. Use the `ls` command to see what's inside of the virutal environment

This shows all of the things that are required for your virtual environment to work.

## Activating Your Virtutal Environment

To begin using our virtual environment, run this command. Type source, the name we gave it, the bin directory, and the activate command.

``` bash
source py3/bin/activate
[py3] $
```

In the example above, the command line prompt changed to show the name of the virtual environment which means that you are now wokring from your virtual environment.

## Installing and Viewing Packages

The whole point of installing and running our virtual environmnet is to be able to download packages in an organized way. So lets do that.

### 1. Use **pip** to install the package/*library* of your choosing. In this example we'll be using the request library

`pip install request`

### 2. To view what packages you've installed, run this command

```bash
pip freeze > requirements.txt
```

This will log the packages/libraries you've installed as well as their version into a txt file called requirements. To see the contents of your requirements.txt and view the packages that have been installed in your command line, run this command:

```bash
cat requirements.txt

certifi==2017.4.17
chardet==3.0.3
idna==2.5
jmespath==0.9.3
requests==2.17.3
urllib3==1.22.1
```

**Why is this a good practice to have?**

It's good to include the requirments.txt file in your directory because you'll want this information to be part of your repo for when/if you push this project to Github.

Now, anyone else who wants to work on your project with you can use `pip install -r requirements.txt` to make sure they have the same library versions as you.

## Exiting Out of Your Virtual Environment

When your done working with your virtual environments, just type deactivate. You're command line prompt should go back to normal.

bash[py3] $ deactivate 
$ python --version

**PRO TIP** Make sure that you don't upload your virtual environment to github. **You want your requirements.txt to be tracked by git but NOT your virtual environemtn**.
