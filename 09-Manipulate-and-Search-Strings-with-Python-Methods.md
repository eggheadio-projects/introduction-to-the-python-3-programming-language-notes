# [Manipulate and Search Strings with Python Methods](https://egghead.io/lessons/python-manipulate-and-search-strings-with-python-methods)

## String Method Format

Using strings is pretty simple. After entering the string or variable name, type dot (.) and then the name of the methods.

## Common String Methods

- endswith
Checks if a string ends with a specified substring. Returns `True` or `False`.

    ```python
    "The ball is red".endswith("red")
    True
    ```

We can also pass in variables as the argument for the `endswith` method.

```python
    my_string ="The ball is red"
    substring = "red"
    my_string.endswith(substring)
    True
```

- find
Checks if a string contains a specified substring. Returns the index number of where the substring is found. If the substring is not found, it will return `-1`.

    ```python
    "The ball is red".find("is")
    9

    "The ball is red".find("foo")
    -1
    ```

- format
Allows us to format strings using positional operators.

    ```python
    "The {0} is {1}".format("ball", "red")
    'The ball is red'
    ```

- join
Accepts a list as the argument and joins list items together.

    ```python
    "".join(["the ", "ball ","is ", "red"])
    'the ball is red'
    ```

- strip, lstrip, and rstrip
`strip` removes all white space. `lstrip` removes all white space on the left side of our string. `rstrip` removes all white space on the right side of our string.

    ```python
    " Will ".strip()
    'Will'

    " Will ".lstrip()
    'Will '

    " Will ".rstrip()
    ' Will'
    ```

## Finding New String Methods

Strings have tons of built in methods available. Use `dir` (which stands for directory) to discover all the methods that can be applied to a string or any other object.

```python
dir("Will")
```

To see how a method works, we can use `help` and pass in the name of the method you're curious about.

```python
help("will".rstrip)
```
