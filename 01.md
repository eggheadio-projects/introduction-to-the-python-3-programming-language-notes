# [Install Python](https://egghead.io/lessons/python-install-python)

---

## Method 1- [Official Python Website](http://python.org/)

To download the latest version of Python, you should visit the official [Python website](http://python.org/). Follow the instructions for your specific operating system.

## Method 2- [Homebrew](https://brew.sh/) for OS X Users

1. Using Homebrew might be easier for OS X users. If you don't already have Homebrew, follow the [directions on this here](https://brew.sh/#install).

2. Once you have Homebrew installed, type this command in your terminal.

``` bash
brew install python3
```

## Method 3- CentOS and AWS Linux

Both have Python 2 by default(more on that later) but not Python3. Follow these steps to install Python3:

1. Install the inline upstream stable package with yum install followed by the path to the IUS package.

    `yum install https://centos7.iuscommunity.org/ius-release.rpm`

2. Now install Python with yum install -y, and specify the name of the Python package which includes the release number. Yours probably won't be Python 3.6. So don't copy this verbatim.

    `yum install -y python36u`

3. You've just installed Python! So use this command to check the exact version you have. And remember, you probably won't have Python 3.6 downloaded.

    `python3.6 -V`

## Method 4- Windows Users

Visit the [Python downloads](https://www.python.org/downloads/windows/) page and follow directions found there for downloading Python on a Windows machine.

## Python 3 vs Python 2

It's best to use Python 3 since it's more modern and it's pretty reliable. Eventhough lots of people still use Python 2, stick to Python 3 unless you have a specific reason to use Python 2.

If you would like to use Python version 2 in your terminal, simply enter `python`.

If you want to use Python version 3 in your terminal, enter `python 3`.
