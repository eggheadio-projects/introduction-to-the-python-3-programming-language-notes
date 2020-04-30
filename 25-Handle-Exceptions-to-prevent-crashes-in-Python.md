# [Handle Exceptions to prevent crashes in Python](https://egghead.io/lessons/python-handle-exceptions-to-prevent-crashes-in-python)

## `try except` Blocks

We don't want our users to confront errors they don't understand. To make sure this doesn't happen, we can use `try except` blocks. This will try a certain block of code and execute a certain block of code if specified exceptions are raised.

Try to make sure that your exception messages are useful and give users insight into what went wrong.

```python
try:
  print(int(sys.argv[1]) / int(sys.argv[2]))
except exception as e:
  print('You must enter a valid number')
```

## Using Multiple Exceptions

In most cases, our code will have multiple exceptions. So we can include multiple `except` statements to catch multiple exceptions.

```python
try:
  print(int(sys.argv[1]) / int(sys.argv[2]))
except ValueError as e:
  print('You must enter a valid number')
except ZeroDivisionError as e:
  print("You can't divide by zero")
```

## Best Practices

- Write your code and make sure to test it afterwards. Once you run your unit tests, create your `try except` block to handle the exceptions you've tested and anticipated.

- Avoid catching all exceptions in one `except` statement. We want our exception messages to be insightful and specific. Catching all exceptions in one go would not be specific enough.

### [Find Built-in Exceptions Here](https://docs.python.org/3/library/exceptions.html)

```python
try:
  print(int(sys.argv[1]) / int(sys.argv[2]))
except exception as e:
  print('You must enter a valid number')
```

## Exceptions for Imported Modules

Modules often have errors that are specific to their purpose. You can usually find this anticipate errors on the module documentation. This makes create unit tests for common errors specific to whatever module you have created.
