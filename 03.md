# [Use Python Interactively with the REPL Console](https://egghead.io/lessons/python-use-python-interactively-with-the-repl-console)

## How do we use REPL?

Just type `python3` into your command line. You can also type `python` for Python 2.

We can treat REPL pretty much like we would our normal text editor. We can type the same commands and see the immediate results of our code.

We can type commands.

```python
print('Hello World!')

```

### Modules in REPL

We can also download modules in REPL. 

```python
import datetime
now = datetime.datetime.now()
print(now)
```

### Functions in REPL

We can create functions in REPL. When we call the function in REPL, we'll be able to see the return value printed to the screen.

``` python
def add(num1, num2):
    return num1 + num2

add(1, 2)

```

## What is REPL?

REPL stands for **R**ead **E**valuate **P**rint **L**oop

Earlier when we typed in `2 + 2`, that was the *read* phase. When pressed enter, `2 + 2` was *evaluated*. Then the answer `4` was *printed* to the screen. Now, you'll notice that we're right back where we started since it automatically *loops* back to the original prompt.

I like to think of it like a cycle which is basically the same thing as a loop.

## Drawbacks of using REPL

REPL is good for testing out code that we want to see immediate results for. But *our code won't be saved in REPL*. So if you want to write code that you would like to reuse, it's best to use your text editor instead.
