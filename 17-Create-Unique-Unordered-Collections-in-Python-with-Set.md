# [Create Unique Unordered Collections in Python with Set](https://egghead.io/lessons/python-create-unique-unordered-collections-in-python-with-set)

## What is a Set?

A set is a collection of items that contains **no duplicates**. Each item in a set is unique.

## How to Create a Set

Start by declaring a varaible. We then create a list of items seperated by commas and wrapped in curly brackets. Even if we include duplicates in our list, it will keep one instance of each item.

```python
animals = {'monkey', 'bear', 'dog', 'monkey', 'cat', 'bear', 'gorilla'}

animals
{'dog', 'cat', 'bear', 'monkey', 'gorilla'}
```

## `in` with Sets

We can use `in` to check if a certain item is contained with a set. Even if we have a large set, this operation works really quickly. Using `in` will return `True` or `False`.

```python
monkey' in animals
True

'shark' in animals
False
```

## Creating Empty Sets

We can't just set a variable equal to curly brackets. That will evaluate to an empty dicitionary. We need to use `set()` to create an empty set.

```python
fish = set()

fish
set()
```

## Set Methods

- add

    We can use add to add things to our set.

    ```python
    fish.add('shark')
    fish.add('guppy')
    fish.add('whale')
    fish
    {'shark', 'whale', 'guppy'}
    ```

- remove

    We can use remove to remove things to our set.

    ```python
    fish.remove('whale')
    fish
    {'shark', 'guppy'}
    ```

- union

    We can use union to combine two different sets.

    ```python
    fish.union(animals)
    {'dog', 'cat', 'bear', 'monkey', 'shark', 'gorilla', 'guppy'}
    ```
