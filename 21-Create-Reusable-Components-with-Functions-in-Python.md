# [Create Reusable Components with Functions in Python](https://egghead.io/lessons/python-create-reusable-components-with-functions-in-python)

## How to Create Functions in Python

We declare functions in Python by using the `def` keyword which stands for define. We follow that with the name of the function and a set of paranthesis.

```python
def say_name():
  print("Heisenberg")

say_name()
```

### Key Things to Remember

- Indentation matters!! The code block the function executes needs to be indented for your function to work the way you want it to.

- Make sure to call the function you create when you would like to use it. It won't execute unless you explicitly called it. I always remember what my Kode With Klossy instructory said, "Always remember to call Katie".

## Return Values in Functions

Even when you don't explicitly use a return in your code, functions always return something. If we don't include a return in our code, Python will return `None` instead.

## Doc Strings

### What is a doc string?

This is a string we include in our function that explains what the function does.

### Why include doc strings?

Including a doc string is considered good practice. It's important to this because doc strings build documentation for your function into the python help system. This become very useful especially when your Python code gets more complex.

```python
def say_name(name):
  """
  Returns name passed in as a paramter
  """
  return name
```

## Scope

```python
def say_name(name):
  """
  Returns name passed in as a paramter
  """
  return name
```

The paramater `name` is local to the scope of the function. That means that outside of the function say_name, Python doesn't know what name is. So `print(name)` would throw an error.

To avoid confusion, don't declare variables outside of your functions with the same name as function paramaters.

```python
def add(num1, num2):
  return num1 + num2

num1 = add(1, 2)
print(num1)
```

This is very bad practice as it's a bit confusing to not confuse the parameter `num1` and the variable `num1`.

## Default Arguments

Our functions can have default arguments which are used if we don't provide an argument when we call on the function.

```python
def add(num1=1, num2=2):
  return num1 + num2

num1 = add()
print(num1)

```

This allows us to call on our function without having to provide arguments.

## Keyword Arguments

We can use keyword arguments when we call on a function. A keyword argument is an argument that is defined when we call on the function.

```python
def madlibs(name, noun="shoes", adjective="red"):
  return "{0} has {1} {2}".format(name, adjective, noun)

madlib = madlibs("Will", noun="boots", adjective="black")
print(madlib)
```

This is a great practice because we can place our keyword arguments in any order and the function will execute the way we want it to. This lowers the likely hood of getting errors in our code.

```python
madlib = madlibs("Will", adjective="black",  noun="boots")
print(madlib)
```

This will still print out `Will has black boots`.

**Remember** once you start using positional arguments, you have to finish out the function still using positional arguments. So this code `madlib = madlibs("Will", Noun = "boots", "black" )` will throw a
`Syntax Error`.

## Positional Arguments

Positional arguments are just arguments without the keyword. So order aka position matters if we want our return value to be formatted correctly.

```python
def madlibs(name, noun="shoes", adjective="red"):
  return "{0} has {1} {2}".format(name, adjective, noun)

madlib = madlibs("Will", "boots", "black" )
print(madlib)
```
