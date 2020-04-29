# [Execute a Python Script](https://egghead.io/lessons/python-execute-a-python-script)

## Creating and Executing a Script

You can create a script by making a python file in your preferred text editor. If you type the `print "Hello World"` for Python 2 or `print("Hello World")` for python three, this what you see you execute the script in your command line...

### Python 2

```bash
python file_name.py

Hello World
```

### Python 3

```bash
python3 file_name.py

Helllo World
```

## Stand-alone Executable Script

To make a stand-alone executable script, use the following in your Python file.

```python
#! /usr/bin/env python

print("Hello world")
```

The important part here is the top line of code which includes `userbin env` which is directed to the Python environment.

Type the following in your command line to execute your new script.

```bash
chmod +x hello.py
./hello.py

Hello world
```
