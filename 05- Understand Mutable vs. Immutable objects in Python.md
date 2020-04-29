# [Understand Mutable vs. Immutable objects in Python](https://egghead.io/lessons/python-understand-mutable-vs-immutable-objects-in-python)

## How We Know If an Object is Mutable

As mentioned in lesson 04, everything in Python has an id and a value. We can use the `id()` function to determine the `ID` of an item.

```python
b = []
id(b)
```

Now to see how `ID`'s play a part in mutability, lets append a number to the `b` list. 

```python
b.append(3)
id(b)
```

We see that the same `ID` was returned for `b` eventhough it's been changed. This means that the list object in Python is mutable, and the same is true for dictionaries.

**So any object that returns the same `ID` value even after it's been altered in some way is *mutable***

## How We Know If an Object is Immutable

The process for checking if an object is immutable is the same. Again use the `id()` function to check the initial `ID` of an item. This time, try it on a variable set equal to a number.

```python
a = 4
id(a)
```

Now perform some sort of operation to change that variable and use `id()` to check the current `ID` of the variable.

```python
a = a + 1
id(a)
```

You'll notice that now `id(a)` returns a different `ID` for `a`. This is because integers are immutable. So immutable objects, however, can't be altered.

Immutable objects in Python include strings, integers, and tuples.
