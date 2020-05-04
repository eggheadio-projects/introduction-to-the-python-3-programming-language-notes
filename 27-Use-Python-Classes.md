# [Use Python Classes](https://egghead.io/lessons/python-use-python-classes)

## Creating a Class

We create classes by using the keyword `class` followed by the name we want to give our class which should be capitalized. 

```python
class Ball:
  color = 'red'
```

### Creating an Instance of a Class

We can create an instance of our class like so:

```python
my_ball = Ball()
```

### Accessing Properties of Instances of Your Class

If we would like to check the properties (for the example, this is `color`) of our class instance (aka `my_ball`). We use dot notation.

```bash
my_ball.color
'red'
```

If we create another instance of `Ball`, the value of the property `color` will also be `red`.

### Default Properties of Your Class Objects

If we want our class instances to be more dynamic and have more properties, we can set default properties which are defined like this:

```python
class Ball:
    def __init__(self, radius, color, weight):
        self.radius = radius
        self.color = color
        self.weight = weight
```

Here the dunder init (`__init__`) method is called when the class is created. We use `self` as an argument. I like to think of `self` as a mirror. The `radius`, `color`,  and `weight` are all attributes of the class.

Calling self in the block of code under our function is like a mirror because it's reflecting whatever we define our attributes as when we create an instance of our class.

```bash
red_ball = Ball(10, 'red', 2)
blue_ball - Ball(12, 'blue', 5)

red_ball.color
'red'

red_ball.weight
2

blue_ball.color
'blue'

blue-ball.weight
5
```

Because we used `self` in our class function, when we create an instance of `Ball`, the properties we pass in are reflected back at use when we call on a property of our instance like `red_ball.color`.

### Instance Attributes vs Class Attributes

When we use default properties, each instance of the class has its own set of properties that can be different from other instances. That's why `red_ball.color` is going to be different from `blue_ball.color`. These are known as instance attributes.

Defining `color = red` in the first `class Ball` created a class instance since each instance of that class will have `color = red` as a property.

## Default Class Methods

We can also give class instances default methods.

```python
class Football:
    """A standard, regulation NFL ball"""
    def __init__(self, diameter, color, pressure):
        self.diameter = diameter
        self.color = color
        self.pressure = pressure
    def inflate(self, psi):
        self.pressure = self.pressure + psi
    def deflate(self, psi):
        self.pressure = self.pressure - psi
```

To call on these default methods, we first create an instance of the class. Then we use dot notation to call on the default method of our choosing.

```bash
bears = Football(22, 'color', 13)

bears.inflate(2)
15

bears.deflate(1)
12
```

## Inheriting Other Classes

Classes can inherit other classes. To do this, create your class with the inherited class as its argument.

```python
class PatriotsBall(Football):
    def inflate(self, psi):
        self.pressure = self.pressure - psi'
```

The `PatriotsBall` class inherits all the properties and functions of  `Football`.

### Overriding Functions Defined in a Class

The function called `inflate` defined in `PatriotsBall` overrides the `inflate` function in the `Football` class.

```python
patriots = PatriotsBall(22, 'brown', 13)

patriots.inflate(2)
patriots.pressure
11
```

Notice when we call on `inflate` it uses the `inflate` function from `PatriotsBall`. It's important to be aware of these behaviors to avoid confusion.

To make sure you know what attributes and methods are in the class that's being inherited, use `dir`.

```bash
dir(PatriotsBall)
['__doc__', '__init__', '__module__', 'deflate', 'inflate']

dir(patriots)
['__doc__', '__init__', '__module__', 'color', 'deflate', 'diameter', 'inflate', 'pressure']
```
