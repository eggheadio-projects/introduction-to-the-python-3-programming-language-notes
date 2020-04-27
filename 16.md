# [Create Immutable Values in Python with Tuples](https://egghead.io/lessons/python-create-immutable-values-in-python-with-tuples)

## What is a Tuple?

Tuples are immutable objects that can hold several items. The items within a tuple do not have to be of the same type.

## How to Create a Tuple

You just declare a varaible and set it equal to the items we want it to hold seperated by commas.

```python
t = 'dog', 'cat', 12345
```

You can wrap them in parenthesis but it's not required.

To access elements inside of the tuple, reference the index just like we do with lists.

```python
t = 'dog', 'cat', 12345

t[0]
'dog'

t[1]
'cat'
```

## Tuples vs Lists

Lists and tuples are very similar. The only real difference is that tuples are immutable. So there are no methods we can perform on tuples that will change the tuple. This includes append, add, extend, and others like that.

## How to Change a Tuple

Tuples are immutable. So technically, we can't change them. If we missed a value in our tuple and wanted to add to it, you have to completely recreate the tuple.

```python
t = 'dog', 'cat', 12345

t = 'dog', 'cat', 12345, 'foo'
```

If we looked at the id on our new `t` tuple, we'll notice that it's different from the original. This is why we tehcnically didn't change our original tuple.
