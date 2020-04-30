# [Read Input in Python from the Console](https://egghead.io/lessons/python-read-input-in-python-from-the-console)

## Input Functions

Input functions allow us to receive input from users. Input functions prompt the user so they can give input and interact with our program.

Input functions are formatted differently in Python 2 and Python 3.

### Python 3 Input Functions

Here's how input functions are formatted in Python 3.

```python
name = input('Name: ')
print(name)
```

### Python 2 Input Functions

Here's how input functions are formatted in Python 2.

```python
name = raw_input('Name: ')
print(name)
```

### Using User Input in Strings

We can use the `format` method to use the user input variables in strings.

```python
name = input('Name: ')
print("Hello, {0}. Nice to meet you!".format(name))
```

We can do this for multiple variables.

```python
name = input('Name: ')
job = input('Occupation: ')
location = input('location: ')

print("Hi {0}, being a {1} in {2} must be exciting!".format(name,job,location))
```

## Input Functions with If Statements

To make our code even more interactive, we can combine input functions with if statements.

```python
response = input('Is it?')

if response in ('yes', 'y', 'yeah'):
  print("How exciting!")
elif response in ('no', 'n', 'nope'):
  print("That's too bad!")
else:
  print("Yeah, I thought so too!")
```

## Input Functions with Integers

All variables we create using input functions are strings. What if we want to as the user for numbers and use those numbers in a math operation? We have to convert the string to an integer using the `int` function.

```python
num1 = input('Enter a number: ')
num2 = input('Enter another number: ')
print(int(num1) + int(num2))
```
