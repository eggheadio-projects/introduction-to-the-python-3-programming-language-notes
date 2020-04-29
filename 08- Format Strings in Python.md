# [Format Strings in Python](https://egghead.io/lessons/python-format-strings-in-python)

## Basic String Declaration

In Python, we declare strings like this: 

```python
name = 'Will'
```

## Double Quotes and Single Quotes

We can use either double quotes ("") or single quotes (''). If our string contains a single quote, we can use double quotes to avoid getting an error.

```python
my_ball = "Will's ball"
```

### Escape Characters

As mentioned, sometimes our strings will contain double or single quotes. We can use escape characters to avoid errors.

- Backslash

```python
    print('Will\'s ball is red')
```

- Triple Quotes

```python
    print("""Will's ball is red""")
```

## Multiline Strings

Python allows us to easily create multiline strings. We use three quotation marks (""") for this.

```python
multiline = """Will's ball
is red
and bouncy!"""
```

When you use multiline strings, the carriage returns are preserved, so that as you print those out, it's returned exactly as you typed it in.

## Substitution Characters

If we assign a string to a variable and we would like to put that variable within a string, we can use substitution characters to do that.

- %s

```python
item = 'ball'
color = 'red'
print("Will's %s is %s." % (item, color))

```

This will return "Will's ball is red."

- format operator

```python
item = 'ball'
color = 'red'
print("Will's {0} is {1}".format(item, color))
```

This will return "Will's ball is red."

`format` is a positional operators. So the number inside of the curly brackets corresponds to the variable in that position.

```python
print("Will's {1} is {1}".format(item, color))
```

This will return "Will's red is red"
