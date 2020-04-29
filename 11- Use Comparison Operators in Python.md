# [Use Comparison Operators in Python](https://egghead.io/lessons/python-use-comparison-operators-in-python)

## Comparison Operators

Comparison operators return `True` or `False`.

- ==

    Checks if a value is equal to another value. Not to be confused with the assignment operator =

    ```python
    5 == 5
    True
    ```

- !=

    Checks that a value is **NOT** equal to another value. So it tests for inequality.

    ```python
    5 != 4
    True
    ```

- \>

    Checks if a value is greater than another value.

    ```python
    5 > 3
    True
    ```

- <

    Checks if a value is less than another value.

    ```python
    3 < 5
    True
    ```

- \>=

    Checks if a value is greater than or equal to another value.

    ```python
    5 >= 3
    True
    ```

- <=

    Checks if a value is les than or equal to another value.

    ```python
    3 <= 5
    True
    ```

## Boolean Operators

Boolean operators are away to evaluate a condition based on two different expresions. Boolean operators return `True` or `False`.

- and

    Returns `True` if **both** specified expressions return `True`.

    ```python
    1 < 2 and 5 > 4
    True
    ```

- or

    Returns `True` as long as at least one of the specified expressions returns `True`.

    ```python
    1 > 2 or 5 > 4
    True
    ```

## Chaining Operators Together

We can chain operators together for more clean and concise code.

```python
x = 4

x > 3 and x < 5
True

3 < x < 5
True
```

## The instance method

We can use the `isinstance` method to compare data types. Returns `True` or `False`.

```python
isinstance("will", str)
True

isinstance("will", int)
False

isinstance(4.0, float)
True
```

## `is` Comparison Operator

The `is` comparison operator checks if two values are the exact same object.

If the object has the same value and it's an immutable object, it will return `True`.

```python
a = True
b = True

a is b
True
```

If the object has the same value but it's a mutable object, it will return `False`.

```python
x = [1, 2, 3]
y = [1, 2, 3]

x is y
False
```

## `in` Comparisom Operator

The `in`comparison operator checks if a value is present within a certain sequence. Returns `True` or `False`.

```python
x = [1, 2, 3]

3 in x
True

5 in x
False
```

## Comparison Operators in Flow Control

Comparison operators are used in flow control very often. Here are some examples of comparison operators being used in flow control. Guess the return value for both.

```python
x = [1, 2, 3]

for value in x:
    if value ==2:
        print('Value is 2!')

car = {'model': 'Chevy', 'year': 1970, 'color': 'red'}

if 'model' in car:
    print('This is a {0}'.format(car['model']))
```
