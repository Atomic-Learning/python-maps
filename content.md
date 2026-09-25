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
def square(x):
    return x * x
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(square, numbers)


for num in squared_numbers:
    print(num)
```

# Creating a List from a Map Object

You can create a list from a map object by passing it to the `list()`{.python} function. For example:

```py-cell
def square(x):
    return x * x
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(square, numbers)

squared_numbers_list = list(squared_numbers)
print(squared_numbers_list)
```

If you want to apply a function to every entry in an iterable and immediately get a list of the results, using `map()` in combination with `list()` is convenient and is significantly more efficient than writing an explicit `for` loop to build the list manually.

# Single Use

If a map is used twice in a row, the second iteration will not produce any results because the map object is exhausted after the first iteration. For example:

```py-cell
def square(x):
    return x * x
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(square, numbers)

# This will print the results of the first iteration
print(list(squared_numbers))

# This will print an empty list because the map is exhausted
print(list(squared_numbers))  
```