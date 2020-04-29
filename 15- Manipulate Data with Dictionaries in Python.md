# [Manipulate Data with Dictionaries in Python](https://egghead.io/lessons/python-manipulate-data-with-dictionaries-in-python)

## What is a Dictionary?

A dictionary is a set of key value pairs. Dictionaries are also known as hashmaps.

Dictionaries are declared like this.

```python
age = {}
```

## Adding Key Value Pairs to Dictionaries

To add to a dictionary, we specify the key we want to add in brackets and set that equal to the value we want.

```python
age['will'] = 40

age['bob'] = 30

age['john'] = 20

age
{'will': 40, 'bob': 30, 'john': 20}
```

## Retrieving Specific Values

We have to call on the key name to access a certain value.

```python
print(age['will'])
40
```

## `in` with Dictionaries

The `in` operator can help us determine if a key exists. This returns `True` or `False`.

```python
'will' in age
True

'austin' in age
False
```

## Dictionaries Methods

- `get`

    We can use the `get` method to retrieve a value from our dictionary. This method accepts two arguments: the key we want the value of and a value to be returned if the key is not found (this is optional).

    ```python
    print(age.get('will', 'Not found'))
    40
    ```

- `del`

    We can delete a specified key value pair with the `del` method.

    ```python
    del age['will']
    ```

- `items()`

    An item is a key-value pair in a dictionary. If we want to retrieve the items in our dictionary, we use the  `items` operator. This is very useful when we are performing a loop on a dictionary.

    ```python
    for key, value in age.items():
        print(key, value)

    ('bob', 30)
    ('john', 20)
    ```
