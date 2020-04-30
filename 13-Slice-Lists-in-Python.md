# [Slice Lists in Python](https://egghead.io/lessons/python-slice-lists-in-python)

## What Does Slicing Do?

Slicing is a way to return a copy of list with just the items that we specify. You specify what items you want returned by providing start and end.

## How Does Slicing Work?

Provide the index you would like the slice to start and the index you would like the index to end at.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]

a[2:5]
[3, 4, 5]
```

### Key Things to Remember

- Lists are indexed starting at zero
- In Python, the item at the end point index is not included

### No End Point

You don't have to specify an end point. If you don't specify an end point, it continues on to the end of the list.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]

a[2:]
[3, 4, 5, 6, 7, 8, 9]
```

### No Start Point

You don't have to specify a start point either. If you don't specify a start point, it starts at the beginning of the list.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]

a[:5]
[1, 2, 3, 4, 5]
```

### Negative Start Point

Negative numbers can be used to start from the end of the list.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]

a[-4:]
[6, 7, 8, 9]
```

### Replacing Items in the List

We can using slicing to replace items in the list. We have to specify the start and end point and set that equal to what ever items we want to be there instead.

Notice that this does not exclude the end point from being replaced.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]

a[2:5] = ['foo', 'bar', 'baz']

a
[1, 2, 'foo', 'bar', 'baz', 6, 7, 8, 9]
```
