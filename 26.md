# [Understand Scope in Python](https://egghead.io/lessons/python-handle-exceptions-to-prevent-crashes-in-python)

## Scope in Nested Functions

A great way to understand scope in functions is to create nested functions that have varaiables of the same name.

Variables are limited to the scope of the function they were created in and any functions created with in their function. It's easier to understand when you see it in code.

Look at the comments for clearer understanding. 

```python
def whoami():
  def local_groot():
    i = "I am local groot"
    ## the i variable above will not be recognized by the whoami() funciton.
  i = "I am groot"
  print(i)
  local_groot()
  print(i)
  # printing i here will not print the i defined in local_groot() since it's scope does not reach whoami()
whoami()
```

This code will print the following.

```bash
I am groot
I am groot
```

Notice, there's no `I am local groot`.

I like to think of functions and their nested functions as celebrities and regular people. Us normal people know everything that goes on in celebrities lives but celebrities don't know anything about us. Functions are the celebrities and nested functions are the normal people.

Adding a `print` statement within the `local_groot()` will allow us to see `I am local groot` printed out since `local_groot()` is called in `whoami()`.

## `nonlocal`

Using the `nonlocal` keyword is a way to override the scope of a variable, making it non-local so that it can be used outside of its scope. We put `nonlocal` in front of the variable we're we want to be non-local.

```python
def whoami():
  def local_groot():
    i = "I am local groot"
    print(i)

  def nonlocal_groot():
    nonlocal i # now this i is non-local meaning it can be referenced in the outer scope function.
    i = "I am nonlocal groot"
  i = "I am groot"
  print(i)
  local_groot()
  print(i)
  nonlocal_groot() # calling this function which includes nonlocal i establishes that that's the i variable we're referencing for the continuation of the function.
  print(i)

whoami()
```

Calling this funtion will return this:

```bash
I am groot
I am local groot
I am groot
I am nonlocal groot
```

Remember that `nonlocal` indicates that a varaiable lives in the enclosing scope. So if we include another `print(i)` in our function, `I am nonlocal groot` will print to the screen again.

## `global`

The `global` keyword allows us to bypass all scope and make any variable available *anywhere* code. It makes the variable an A-list celebrity that everyone knows.

```python
def whoami():
  def local_groot():
    i = "I am local groot"
    print(i)

  def nonlocal_groot():
    nonlocal i
    i = "I am nonlocal groot"

  def global_groot(name):
    global i
    i = "I am global groot"

  i = "I am groot"
  print(i)
  local_groot()
  print(i)
  nonlocal_groot()
  print(i)
  global_groot()
  print(i)

whoami()
print(i)
```

This is what this function returns:

```bash
I am groot
I am local groot
I am groot
I am nonlocal groot
I am nonlocal groot
I am global groot
```

You notice that even though we called on `global_groot()`, `I am nonlocal groot` prints twice. That's because calling `nonlocal_groot` sets the value of `i` to `I am nonlocal groot` for the remainder of the function since we are still in the enclosed scope of `whoami()`.

But when we call `print(i)` outside of the `whoami()` function `I am global groot` is printed because it is now a global variable.

**REMEMBER** USING GLOBAL SCOPE VARIABLES LIKE THIS IS NOT BEST PRACTICE!! Because it's so confusing, it's better to override scope using parameters.

### BEST PRACTICE: Using Parameters Instead of `global`

Use a parameter for when you call on your nested function instead of using `global`.

```python
def whoami():
  def local_groot():
    i = "I am local groot"
    print(i)

  def nonlocal_groot():
    nonlocal i
    i = "I am nonlocal groot"

  def global_groot(name):
    return "I am {0} groot".format(name)

  i = "I am groot"
  print(i)
  local_groot()
  print(i)
  nonlocal_groot()
  print(i)
  print(global_groot("the only"))
  print(i)

whoami()
```

This will print:

```bash
I am groot
I am local groot
I am groot
I am nonlocal groot
I am the only groot
I am global groot
```
