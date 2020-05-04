# [Reuse Code in Multiple Projects with Python Modules](https://egghead.io/lessons/python-reuse-code-in-multiple-projects-with-python-modules)

## What is a Module?

A module is a function we use in our code that comes from another file. We do this to make our life easier and to keep our code DRY. This also makes team collaboration easier as other developers can just use your module instead of having to copy all of your code.

## How Do We Use Modules?

Say there is a Python file called `tax.py` that contains the following code:

```python
def total(n):
  tax_rate = .07
  return n * tax_rate + n
```

If we would like to reuse this code in our own Python file, we have to `import` it. At the top of our file, we `import` the module we want to use aka `tax.py`. We don't have to include the file extension .py.

When we're ready to use the module, we call on the module name followed by a period (.) followed by the name of the specific function we want to use.

### Importing in the Terminal

This is what importing looks like in the terminal:

```bash
import tax

print(tax.total(5))
5.35
```

### Importing in the Text Editor

This is what importing looks like in the text editor:

```python
import tax

print(tax.total(5))
```

## Using Modules Without Importing

Usually, our modules are only accessible when we import them. We can bypass this behavior though. Then we can execute modules as standalones instead of importing.

Here's how we go about executing modules in a standalone fashion:

```python
if __name__ == "__main__":
  import sys
  print(total(int(sys.argv[1])))
```

Now if we run this command in the terminal, `python3 tax.py 10` we get a result without having to import anything.

## Only Importing Functions that We Need

Say the `tax.py` file we've been importing from has another funtion `tax_amount`.

```python
def tax_amount(n):
  tax_rate = .07
  return n * tax_rate
```

If we only want to use one function from the `tax` module, we can type the following in our code:

```python
from tax import tax_amount

# print(tax.total(7))
print(tax_amount(7))
```

Using the `from` syntax means we're only using what we need which reduces the memory footprint and load time of your Python code. This makes your code faster.
