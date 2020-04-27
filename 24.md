# [Write to a File in Python](https://egghead.io/lessons/python-write-to-a-file-in-python)

We can also create files from within our Python code.

## Creating a Text File With Python

We'll need to use the `open` method to do this. This will create a new file outside of our Python code and put whatever contents we specify.

```python
f = open('cars.txt', 'w')
cars = ['chevy', 'tesla', 'ford']
  for car in cars:
    f.write(car + '\n')
```

### Using the `close` Method

Again, we should use the `close` method to close the file as soon as our code finishes executing.

```python
f.close()
```

### Using `with` Blocks

We can also use `with` blocks for this.

```python
with open('cars.txt', 'a') as f:
  cars = ['chevy', 'vw', 'mazda']
  for car in cars:
    f.write(car +'\n)
```

## Creating JSON Files

We can also create an external JSON file in our Python code. Start by creating a JSON object in your code.

```python
cars = [
  {"make": "chevy"},
  {"make": "tesla"},
  {"make": "porsche"}
]

import json
with open('cars.json', 'w') as f:
  json.dump(cars, f)
```
