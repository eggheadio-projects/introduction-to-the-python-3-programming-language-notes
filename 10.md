# [Add Flow Control to your Python application](https://egghead.io/lessons/python-add-flow-control-to-your-python-application)

## If Statements

This is a type of flow control statment in Python. Here is an example of how if statements work in Python.

```python
x = int(input("enter an integer: "))

if x < 0:
  x = 0
  print("Negative number changed to zero")
```

### Elif

We can expand our if statements by adding more conditions using `elif` which stands for else if.

```python
x = int(input("enter an integer: "))

if x < 0:
  x = 0
  print("Negative number changed to zero")
elif x == 0:
  print("zero")
```

### Things to Remember When Creating If Statements

- Make sure to check all possible cases and outcomes for your if statements to make sure the code is executing the way it should

- Also don't forget the : after the if statement. If it's not there, you'll get an error and the code won't work.

- Indentation matters in Python. So make sure that the code blocks that execute when a codition is met are indented properly.

## For Loops

For loops are used to iterate over any kind of sequence like lists or strings. There are two types of for loops.

1. for in

    ```python
    pets = ['cat', 'dog', 'elephant']

    for pet in pets:
        print('I have a pet {0}'.format(pet))
    ```

    Basically, for initiates a loop that iterates over each item in the `pets` array. Each item is represented by the temporary variable `pet`. The loop is going to execute the code block for each `pet` inside `pets`.

2. for in range

    ```python
    for i in range(5):
        print(i)
    ```

    This for loop uses the `range` operator. Using `for i in range` will increment up to *but not including* the specified number in the paranthesis.

    ```python
    for i in range(10, 15):
        print(i)
    ```

    We can have two arguments that point the starting point and ending point in the range if we want. For the example above, 10 is the starting point and 15 is the ending point.

    ```python
    for i in range(0, 10, 2):
        print(i)
    ```

    We can also include a third argument which specifies the increment that the numbers will increase by. In the example above, the loop starts at 0 and increase by two.

    ```python
    for i in range(10, 0, -1):
        print(i)
    ```

    We can also decrement which is done in the for in range loop above.

## While Statements

While statements create loops that run as long as a specified condition is true.

```python
x = 1

while x < 10:
    print(x)
    x = x + 1
```

`x` acts as our counter.

## Break Statements

```python
pets = ['cat', 'dog', 'elephant']

for pet in pets:
    if pet == 'dog':
        print('No dogs allowed')
        break
    else:
        print('We love {0}!'.format(pet))
```

All of the loop statements with the exception of while will continue to iterate and loop until they've reached the end of their given sequence. To bypass this, we can use a *break statement*

In the code example, the for loop goes over `'cat'` and `'dog'` and then `break`s once dog is reached because of the `break` statement within the if statement. So `'elephant'` is never reached.
