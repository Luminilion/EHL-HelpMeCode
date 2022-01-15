# Ex 0

Describe the differences between these types:
- `list`
- `dict`
- `tuple`
- `set`

Which one adds an element at a given position in the list ?
Which one gives us the last element ?

- [ ] `list.sort()`
- [ ] `list.pop()`
- [ ] `len(list)`
- [ ] `list.remove(4)`
- [ ] `list.insert(4, 2)`
- [ ] `list.append(4)`

What will this code return ?
````
batman = 'Bruce Wayne'

var1 = {
    'car':'ford',
    'color': 'blue',
    'price' : 10,
    'age': 15,
    'owner' : batman
}

value = var1['price'] * var1['age'] * len(var1['owner'])
print(f"The value is {value}.")

secret = var1['color'][1] + var1['car'][1] + var1['color'][1]
````

# Ex 1

Which function is built-in and which one is not ?

````
1. list = [1, 2, 3, 4, 2]
2. def function1():
3.     print('This is function one!')
4. my_variable = "Weather forecast"
````

- [ ] `list.append(1)`
- [ ] `type(my_variable)`
- [ ] `len(list)`
- [ ] `my_variable[2].lower()`

# Ex 2

Do the following:
- Create a **function** that computes the product of 2 numbers.
- Create a **function** that prints "This is big" if the input number is bigger than 10.
- Declare a **list** of numbers from 4 to 10.
- Store in **another variable** all even elements from the list (1 out of 2 elements).
- Multiply the first and the last element of the second list using the `product function`.
- Pass the result to the function checking if it is big.

# Ex 3

Find all errors in this code and tell which type they are (coding mistake, runtime error, logical error).

````
# Objective: Create a function to compute an element to the power of a number.

def power(a b):
    result = 0
    for i in range(b) :
        result = result * a
    return result
    
my-first-element = 3
elementB = 2

myResult = power(my-first-element, elementB)
print("Wow the result is " + myResult)
````

# Ex 4

What does this code do ?

````
function1 = lambda x : x + 1
result = function1(3)
print(result)
````

# Ex 5

Which ones are correct ?

````
1. myList = [2.45, 4.83, 5, 10]
2. myCars = ['Ford', 'Mitsubishi', 'BMW', 'VW']

3. def sorting_by_length(e):
4.     return len(e)
````

- [ ] `sorted(myList, reverse='1')`
- [ ] `myList.sort()`
- [ ] `myCars.sort(key=sorting_by_length)`
- [ ] `sorted(myCars, reverse=True)`