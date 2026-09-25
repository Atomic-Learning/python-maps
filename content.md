A `map`{.python} is an object in Python which contains a reference to a function and an iterable (such as a list). The `map`{.python} object is itself iterable and returns the values returned when the function is applied to the elements of the iterable object.

# Creation

To create a map object, use the `map()`{.python} function, passing in the function and the iterable as arguments. For example:

```py-cell
# Create a function
def square(x):
    return x * x

# Create a list
numbers = [1, 2, 3, 4, 5]

# Create a map object
squared_numbers = map(square, numbers)
```

Note that the `map`{.python} object does not calculate the results immediately.

# Iterating Over a Map Object

We can iterate over a map object using a `for` loop, just like any other iterable. For example:

```py-cell
# Make sure to the run the first cell on the page first
for num in squared_numbers:
    print(num)
```

# Creating a List from a Map Object

You can create a list from a map object by passing it to the `list()`{.python} function. For example:

```py-cell
# Make sure to the run the first cell on the page first
squared_numbers_list = list(squared_numbers)
print(squared_numbers_list)
```

If you want to apply a function to every entry in an iterable and immediately get a list of the results, using `map()` in combination with `list()` is a convenient and efficient approach.