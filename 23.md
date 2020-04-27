# [Read and Parse Files in Python](https://egghead.io/lessons/python-read-and-parse-files-in-python)

Python is great for parsing through and processing information from different file types.

## How to Parse Files in Python

We use the `open` method to return file objects. This makes it easy to work with other file types. We just have to specify what file we would like to work with.

```python
f = open('animals.csv')
```

### Mode

There are different modes we can process file information in.

- `r`

    This stands for read and is the default if we don't specify in our code.

    ```python
    f = open('animals.csv', 'r')
    ```

- `w`

    This stands for write. This rewrites the file contents with whatever we specify in our code. Whatever was in the file is no longer there.

    ```python
    f = open('animals.csv', 'w')
    ```

- `a`

    This stands for append. This adds whatever we specify in our code to the existing file contents. So nothing is taken away.

    ```python
    f = open('animals.csv', 'a')
    ```

## Using File Objects

`f` is a file object. We can now execute functions and for loops on `f`.

```python
f = open('animals.csv')

for line in f:
  print(line)
```

## Close Method

When we're parsing long-running files, we'll need the `close` method to close out the file. Without this, the file will stay open and take up memory.

```python
f = open('animals.csv')

for line in f:
  print(line)

f.close()
```

## With Block

With blocks are great because they automatically close the file once the code is done executing. So you don't have to explicitly call the `close` method.

```python
with open('animals.csv', 'r') as f:
print(f.read())
```

## Building More Complex Code with File Parsing

We can make our code more complex by import the file module for whatever file type we're dealing with if it's available. So for the examples, that means `import csv`.

### Complex Code with csv Files

```python
import csv
with open('animals.csv', 'r') as f:
  animals = csv.reader(f)
  for row in animals:
    if row[-1] == 'True':
        print("{0} is a {1} and is  housebroken".format(row[0], row[1]))
    elif row[-1] == 'False':
        print("{0} is a {1} and is not housebroken!".format(row[0], row[1]))
```

### Complex Code with JSON files

```python
import json
with open('animals.json', 'r') as r:
  data = json.load(r)
  for row in data:
    print(row['name'])
```

Test the code to see the results.
