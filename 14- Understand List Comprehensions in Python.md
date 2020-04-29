# [Understand List Comprehensions in Python](https://egghead.io/lessons/python-understand-list-comprehensions-in-python)

## What is List Comprehension?

For loops are often used to parse through lists and create new ones. List comprehension allows us to make this code cleaner and more concise.

### Without List Comprehension

```python
zoo_animals = ['giraffe', 'monkey', 'elephant', 'lion','bear', 'pig', 'horse', 'aardvark']

my_animals = ['monkey', 'bear', 'pig']

not_my_animals = []

for animal in zoo_animals:
    if animal not in my_animals:
        not_my_animals.append(animal)

not_my_animals
['giraffe', 'elephant', 'lion', 'horse', 'aardvark']
```

### With List Comprehension

```python
zoo_animals = ['giraffe', 'monkey', 'elephant', 'lion','bear', 'pig', 'horse', 'aardvark']

my_animals = ['monkey', 'bear', 'pig']

other_animals = [animal for animal in zoo_animals if animal not in my_animals]

other_animals
['giraffe', 'elephant', 'lion', 'horse', 'aardvark']
```

As you can see, the code with list comprehension is  shorter.

## How List Comprehension Works

List comprehension is basically a condensed loop.

```python
sales = [3.14, 7.99, 10.99, 0.99, 1.24]

sales2 = [sale * 1.07 for sale in sales]

sales2
[3.3598000000000003, 8.5493, 11.759300000000001, 1.0593000000000001, 1.3268]
```

**Here's the step by step for creating performing list comprehension**

1. Declare a temporary variable (just like we do with for loops)

    ```python
    sales2 = [sale ]
    ```

2. Apply whatever operation we want to the temporary variable

    ```python
    sales2 = [sale * 1.07]
    ```

3. We then include a for statement.

    ```python
    sales2 = [sale * 1.07 for sale in sales]
    ```

## Complex List Comprehensions

List comprehensions can get confusing, especially when they're more complex. There is a way to help cut down on confusion.

**Not so easy way**

```python
other_animals = [animal for animal in zoo_animals if animal not in my_animals]
```

**Easy way**

```python
other_animals = [
    animal
    for animal in zoo_animals
    if animal not in my_animals]
```

Breaking the list comprehension up on different lines can make the code easier to understand.

Both ways give us the smae return value.

```python
other_animals
['giraffe', 'elephant', 'lion', 'horse', 'aardvark']
```
