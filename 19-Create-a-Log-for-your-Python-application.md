# [Create a Log for your Python application](https://egghead.io/lessons/python-create-a-log-for-your-python-application)

## Creating Logs in Python

First import the logging module. Once we do that, you can type the following to log a message.

```bash
import logging
logging.warning('This is a warning')

WARNING:root:This is a warning
```

## Logging Levels

There are different levels of severity in logging. The example above logged a warning message. The levels, in order of most severe to least, are **critical, error, warning, info, and debug**.

When importing `logging`, the default is warning. Any level below warning will **NOT** be returned in the terminal.

## Practical Use of Log

When using `logging` in a project, you of couse start by importing `logging`. Then you have to configure it.

```python
logging.basicConfig(filename='./demo.log', level=logging.DEBUG
```

This code is configured to write to a file name (aka `demo.log`) and sets the logging level to debug.

Here's how it looks using logs in a loop.

```python
for i in range(0, 100):
  if i % 5 == 0:
    logging.debug('Found a number divisible by 5: {0}'.format(i))
  else:
    logging.info('At number {0}'.format(i))
logging.warning('Finished sequence')
```

## Specify Log Level on the Command Line

To be able to specify the log level on the command line, we need import both the `sys` (allows us to read the command line arguments) and `getopt`(makes parsing command line arguments easier) modules.

Read the comments in the code for more info.

```python
import sys
import getopt
import logging

log_level="INFO"

opts, args = getopt.getopt(sys.argv[1:], "l:", ["log="])
# created variables opts and args. Call on getopt to parse sys.argv aka system arguments
# slice the list to exclude first arg and look for 2 params, either l or log=

for opt, arg in opts:
    if opt in ("-l", "--log"):
        # if this evaluates to true, indicates log level parameter given to our application
        log_level = getattr(logging, arg.upper())
        # gets the numerica value of the level passed in

logging.basicConfig(filename='./demo.log', level=log_level, format='%(asctime)s %(levelname)s:%(message)s')
# notice that level is changed to machine the log_level variable created in the loop.
```
