# [Invoke the built-in help system with python's dir and help methods](https://egghead.io/lessons/python-invoke-the-built-in-help-system-with-python-s-dir-and-help-methods)

## How to Figure Out What Methods Are Available to an Object

We can use the `dir` method to determine what methods are available to an object. `dir` will return a list of all the methods we can use with a specified object.

```python
"foo"

dir("foo")
```

## How to Figure Out How to Use a Method

We can use `help` for figuring out how a method should be used and what it should be used for. `help` will return a quick summary of what the method can do.

```python
help("foo".upper)
```
