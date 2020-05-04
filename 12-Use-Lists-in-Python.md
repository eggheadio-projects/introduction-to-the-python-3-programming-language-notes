# [Use Lists in Python](https://egghead.io/lessons/python-use-lists-in-python)

## Creating Lists

Lists are a sequence of objects. Objects don't have to be of the same type either.

```python
a = [1, 2, 3, 4]

b = [1, 'cat', 7, {'car': 'chevy'}]
```

## Index

We can access items in lists by calling on their index. The index of the first item is `0` and goes up from there.

```python
b = [1, 'cat', 7, {'car': 'chevy'}]

b [0]
1

b[1]
'cat'
```

## Common List Methods

- `append`
    
    The `append` method adds an item to the end of the list

    ```python
    pets = []

    pets.append('cat')
    pets.append('dog')
    pets.append('bear')
    pets.append('shark')

    pets
    ['cat', 'dog', 'bear', 'shark']
    ```

- `remove`

    The `remove` method removes a specified item from the list

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    pets.remove('dog')
    ```

- `pop`

    The `pop` method removes the last item from the list

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    pets.pop()
    'shark'
    ```

    If we want to remove a specific item from the list, we can input the index of the item.

- `sort`

    The `sort` method sorts the items in the list alphabetically.

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    pets.sort()
    ['bear', 'cat', 'dog', 'shark']
     ```

- `reverse`

    The `reverse` method puts the items of the list in reverse order.

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    pets.reverse()
    ['shark', 'dog', 'cat', 'bear']
    ```

- `len`

    The `len` method returns the amount of items in present in the list.

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    len(pets)
    4
    ```

- `count`

    The `count` counts how many times an item is present in a list.

    ```python
    pets = ['cat', 'dog', 'bear', 'shark']

    pets.count('bear')
    1
    ```
