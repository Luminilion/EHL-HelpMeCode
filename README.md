# Cheatsheet Python EHL
A l’attention de Mlle A.C.

## Basics that he did not include

**What is code?** <br>
Code must be seen as a recipe. It is a series of instructions that the computer is going to execute one after another. It always goes from top to bottom. It does not see what is after the code that it just read. But it remembers everything that it read before.

```
1. print("Hello you")
2. 123
3. print(123)
4. 10 + 10
5. print(10 + 20)
############# Outputs ###############
Hello you
123
30
```
Line ``2.`` did not do anything because it is as if I told the computer the number "123", it does not know what to do with it so it ignores it. If I tell it `print(123)` then it knows what to do and prints "123".
Same for line `4.`, I am just telling the computer "hey, 10 + 10", and so it calculates ``10 + 10`` and then does not know what to do out of it. But line `5.` tells him to `print(10 + 20)`, so it calculates `10+20` and then `print` the result.

**What is a variable?** <br>
A variable is like a box. This box is in the memory of the computer. So when you put a value in the box (i.e. in the variable) the computer remembers it. You can use this values again later on by calling the box (i.e. the variable). The box can have any name you choose (without spaces).

```
1. print("Hello you")

2. my_little_variable = "Hello me"
3. aaaaaaaaaaaaaaa = 123456789

4. print(aaaaaaaaaaaaaaa)
5. print(my_little_variable)
############# Outputs ###############
Hello you
123456789
Hello me
```

Line `2.` and `3.` stored the values `"Hello me"` and `123456789` into the boxes `my_little_variable` and `aaaaaaaaaaaaaaa`. And then line `4.` and `5.` called the boxes to get their values back to print them.

**What are types?** <br>
A type is the nature of a value. There are 4 basic types :
- `int`: any integer number. Ex: `1` or `800` or `-45`.
- `float`: any decimal number. Ex: `2.87` or `1000.0` or `-0.00394362836`.
- `bool`: boolean value. This is a value that is binary i.e. it can either take value `True` or `False`. See this as *Yes* or *No*. Ex: `True` or `False` (nothing else really).
- `char`: any character. See this as a *letter*. It must always be in quotation marks. Ex: `'a'` or `'\'` or `';'`.

And then you can compose an actual *text* by adding up multiple `char` values. This becomes another type:
- `str`: string value. See this as *text*. Ex: `"a\;"` or `"Hello"` or `"12abc"`.

Note: For `str` or `char`, simple quotation `''` or double `""` are the same.

Note2: For `bool`, you can write an expression that is going to be executed by the computer to see if it ends up being `True` or `False`. Ex: `12 > 11` is going to be executed as `True` by the computer. But `10 > 11` is going to be executed as `False`. Ex:

```
my_variable = 10 > 11
print(my_variable)
############# Outputs ###############
False
```

## Structure of Python File

**What is a package?** <br>
A package is a bunch of files containing code written by someone else. You can re-use the code by *importing* it in your own code. Example: *statistics* package contains everything related to statistical computations. It spares you from re-writing the calculations for an average, a standard deviation…

*Metaphor:* See a package as a gardener. He contains a lot of knowledge about plants. If you want to grow plants, you can either ask him to explain to you precisely how to grow plants. Or you can just tell him to grow plants in your garden. The first thing implies you have to redo everything he tells you. The second implies that you just tell him what you want to grow and he'll do it. <br> Well the first case is writing all the code by yourself and the second case is just using a package and telling the package to do some specific things (e.g. grow a plant).

**How to use a package?** <br>
You must import it into your code (otherwise your code does not know where all the knowledge is). There are multiple ways:

```
1.  import statistics
2.  from statistics import average
3.  import statistics as st
```

- ``1.`` simply imports the package called ``statistics``. This means that you can use the code from the package in your code. Usage: ``statistics.average()``
- ``2.`` imports only the bunch of code called ``average`` from the package ``statistics``. Usage: ``average()``
- ``3.`` imports the package called ``statistics`` but gives it a little name ``st`` so that in your code you can simply write ``st`` and not statistics every time you want to use a bunch of code from the package. Usage: ``st.average()``

**What is a comment?**<br>
A comment is a bunch of code that is not going to be executed by the computer. It is here if you want to write explanations in english (or french or whatever) in the middle of your code. Everything on the right of the `#` on the same line will not be executed.
```
1. blabla() # This code launches a nuclear war
2. blabla2() # This code does a great drawing
```

**What is indentation?** <br>
Indentation is the fact of writing with some space between the code and the left margin. Example:<br>
```
1. somecode1() #This is not indented
2.  somecode2() #This is indented once
3.    blabla() #This is indented twice
4.    blabla2() #This is indented twice
5.  somecode3() #This is indented once  
```
If a code line is indented, it means that it depends on the previous non indented code line. Here ``blabla()`` and ``blabla2()`` depend on ``somecode2()``. And `somecode2()` and `somecode3()` depends on `somecode1()`. <br>This means we can talk about *blocks of code*. All the lines that are indented the same or more are part of the same block. Here lines `3.` and `4.` form a block of code (because they are indented the same). And similarly, lines `2.`, `3.`, `4.` and `5.` form another block of code (because they are indented the same or more).

You can indent by pressing the ``tab`` key.

**What is ``if __name__ == '__main__'``?**<br>
Forget about this, it's useless for you and implies complicated stuff. Ask me if you really want to understand.

## `if` statements

<span style='color:red'> What is `if`?**
`if` is a special code word in Python. It is used like this:
```
1. if conditionA :
2.    blabla()
3.    blablabla()
4. blabla2()
```

Let us decrypt this. `conditionA` is a variable with a `bool` value. It must always be a boolean value so that it contains `True` or `False`. Then depending on if it is `True` (see this as *Yes*) or `False` (see this as *No*), the computer is going to enter the `if` or not.
*Enter the if* means that the computer executes the block of code dependent on the `if` line. <br>
So in our case:
- the `if` line is line `1.`
- the block of code depending on it is lines `2.` and `3.`
- line `4.` does not depend on the `if` line because it is indented the same as `1.` and not more.

So the computer is going to read line `1.`, check if the box `conditionA` contains `True`. If it does, it will execute the lines `2.` and `3.`. If `conditionA` contains `False`, it will not execute the block of `2.` and `3.`. Then it will always (regardless of `conditionA`) execute line `4.`.

Example:

```
1. conditionA = 10 > 11
2. if conditionA:
3.    print("The if was executed!")
4. print("I am always executed")
############# Outputs ###############
I am always executed
```

So in our example, `conditionA` contains `10 > 11` which is `False`. So the computer does not enter the `if` and does not execute line `3.`. But it executes line `4.`.

**What if I want to do something else if `conditionA` is not true?**

You can use the `else` code word. The computer is going to enter the `else` if it did not enter the `if`.

```
1. conditionA = 10 > 11
2. if conditionA:
3.    print("The if was executed!")
4. else:
5.    print("The else was executed instead!")
6. print("I am always executed")
############# Outputs ###############
The else was executed instead!
I am always executed
```

Here `conditionA` is `False` and therefore the `if` is not entered. So the computer enters the `else` instead. The block depending on `else` is line `5.` because it is indented.

**How can I do different things for different conditions? **

You mean that you want to do something if `conditionA` is True, but something else if `conditionB` is True and something else if both are false ?

Ok let us do this using the word `elif`. This word is a mix between `else` and `if`. It means "*if the previous condition is false, try me! But I have a condition as well*". Ex:

```
1. conditionA = 10 > 11
2. conditionB = 12 > 11

3. if conditionA:
4.    print("The if was executed!")
5. elif conditionB:
6.    print("The elif was executed!")
7. else:
8.    print("The else was executed instead!")

9. print("I am always executed")
############# Outputs ###############
The elif was executed!
I am always executed
```

What happened?<br>
- Well first let us look at the conditions. `conditionA` is still `False`. But ``conditionB`` is ``True`` (yes 12 is bigger than 11).
- So the `if` is going to check if `conditionA` is `True`. But it is not, so we skip line `4.`
- And arrive to line `5.`, where there is another ``conditionB``. This one is ``True``! So the computer enters the ``elif``.
- The computer executes line `6.` and continues.
- Line `7.` is skipped because one of the previous conditions was verified.
- Line `8.` is skipped because line `7.` on which it depends is skipped.
- Line `9.` always executes because it's independent!

Note1: this kind of multiple choice always starts with `if`. Then there may be ``elif`` and ``else`` statements (or maybe not).

Note2: There can only be one `if` or `elif` or `else` that is entered by the computer. Once it is done all the following are skipped even if the conditions are `True`.

Note3: Consider the `else` as the trash. If no condition is `True`, well the computer always ends up entering the `else`.

**How can I do more complicated conditions ?** <br>

You can verify more than one condition in the `if`. To do this, you can combine your conditions with `or` and `and`. You can also transform them with `not`.

- `not` switches the value. If it is `not True`, the computer understands `False`. And if it is not `not False`, the computer understands `True`.
- `and` puts two boolean values together. Both values must be `True` for the result to be `True`.
- `or` puts two boolean values together. But here at least one of the values must be `True` for the result to be `True`.

```
1. conditionA = 12 > 11
2. print(conditionA)

3. conditionB = not True
4. print(conditionB)

5. conditionC = True and False
6. print(conditionC)

7. conditionD = True or False
8. print(conditionD)
############# Outputs ###############
True
False
False
True
```

Let us check a more complicated example.
```
1. conditionA = 12 > 11
2. conditionB = not ConditionA
3. print(conditionB)

4. conditionC = not (conditionA or conditionB)
5. print(conditionC)
############# Outputs ###############
False
False
```

Ok let us understand this.<br>
- Line `1.` puts `True` in the box `conditionA`.
- Line `2.` puts the inverse (`not`) of `conditionA` into `conditionB`. So it puts `not True` i.e. it puts `False`.

- Line `4.` puts `not (...)` into `conditionC`. But what is `not (...)`?
  - Well `(...)` is `conditionA or conditionB`. So it is `True or False`. We know that `or` checks if at least one of the two values is `True`. It is! So `conditionA or conditionB` outputs `True`.
- Now we know that `not (...)` is `not True`. And that `not` inverses the value. So `not (...)` outputs `False`. So after having calculated everything that is on the right of line `4.`, the computer puts `False` into `conditionC`.


## Functions

This is starting to get more serious here. But first... <br>
**What are functions ?**

*Functions* are like variables, they contain a value and you can call them (i.e. you can write their names to get their values). But they don't contain a single value in their box, they contain a whole bunch of code. So you can think of it like giving a name to a block of code.

In short, when you call functions, you call all the code that is inside them. So with a single line, you can execute multiple lines of code. Here is what it looks like :

````
1. def my_first_function() :
2.     a = "Hello"
3.     b = "you!"
4.     print(a + b)

5. my_first_function()
############# Outputs ###############
Hello you!
````

Let's understand this:
- Line ``1.`` creates the function. It uses the special word ``def`` (short for *definition*) to indicate that what follows is a function. Right after ``def`` comes the name of the function (here it is ``my_first_function``). And then finally there are the parenthesis ``()`` to give input values to the function. Here we don't need any input values so the parenthesis are empty.
- Lines ``2.`` and ``3.`` are indented. So this means that they depend on the previous line. Here of course they depend on the function. So the block of code lines ``2.`` and ``3.`` are the code that is going to be executed when someone calls the ``my_first_function`` function.
- Finally line ``5.`` calls the function. So we write the name of the function and the list of values we give to it as input. But here we don't need to give any because when we created the function at line ``1.`` we didn't put any in the parenthesis. Calling the function will go to the definition of the function (so to line ``1.``) and will execute all the lines that depend on it (here lines ``2.`` and ``3.``).

**What are the input values ?**

Ok you probably got it but didn't quite understand the input values. Well they are called *arguments* or *parameters*. They give the possibility to pass on something to the function when you call it.

Imagine that you want to write a long email and want to change the name of the person receiving the email. It's a pain to rewrite everything everytime. So we can define a function that takes the name as input value and then just writes the same message.

````
1. def write_email(name) :
2.    greeting = "Hello "
3.    message = ", I am sending you this email to blablablabla...."
4.    full_email = greeting + name + message
5.    print(full_email)

6. write_email("Donald Trump")
7. write_email("Barack Obama")
8. write_email("Joe Biden")
############# Outputs ###############
Hello Donald Trump, I am sending you this email to blablablabla....
Hello Barack Obama, I am sending you this email to blablablabla....
Hello Joe Biden, I am sending you this email to blablablabla....
````

See ! This enabled us to write the 3 emails in 3 lines (``6.``, ``7.`` and  ``8.``) instead of each time rewriting lines ``2.``, ``3.``, ``4.`` and ``5.``.
And each time, we could indicate to the function what we wanted to change.

So to conclude, *arguments* allow us to input values in the function when we call them. So that some things can change inside the function without us rewriting the whole code.

**What if I want to get something out of my function?**

You may want to do something else than just printing values (this is great but does not help you very much because you cannot do anything with the thing that is printed).

To actually get something out of the function you can use the ``return`` special word. It is used at the end of the function always to give back something to the user.

Imagine I want to compute the average of 2 values. I am not going to write always the calculation ``(a + b)/2``. It's too long. So we can define a function that calculates this and gives us back the result.

````
1. def average(a, b):
2.     sum = a + b
3.     average = sum / 2
4.     return average

5. average(2, 2)
6. print(average(11, 1))
7. print(average(-4, 4))
############# Outputs ###############
6
0
````

Did you get it ? Here is what happened:
- line ``1.`` created the function called ``average`` taking 2 arguments ``a`` and ``b``.
- lines ``2.`` and ``3.`` do the calculations to get the average of the two values ``a`` and ``b``.
- line ``4.`` gives back the result of the calculation.

- line ``5.`` calls the function with ``2`` and ``2`` (so when the function executes ``a = 2`` and ``b=2`` in the calculations). And then the result of the functions is ``2`` (yes the average between 2 and 2 is 2). But we don't tell the computer to do anything out of it.
- line ``6.`` however calls the function ``average`` with arguments ``11`` and ``1``. So the computer goes to the definition of ``average`` on line ``1.`` and then executes all the lines that depend on it (``2.``, ``3.`` and ``4.`` here). Then it finds a result of ``6`` (you can check by yourself). So ``average(11, 1)`` in line ``6.`` equals to ``6``. And we tell the computer to ``print(average(11, 1))`` so it ``print(6)`` and we get a ``6`` displayed.
- same goes for line ``7.``.

And then you can do a bunch of really complicated things in a function. But usually, they are used to *clean the code* (i.e. make it more understandable) or to *avoid rewriting the same code if you do multiple times the same thing*.

Note1: With functions, you can use the code in the *packages* that we saw at the beginning for example! Imagine the package ``statistics`` has a function average, then you don't have to rewrite it yourself to calculate an average. You can simply do :

````
1. import statistics as st

2. my_average = st.average(11, 1)
3. print(my_average)
############# Outputs ###############
6
````

See? We used the function ``average`` that is in the *package* (bunch of code written by someone else) ``statistics``.

Note2: There exist some functions that don't need any ``import``. You can just use them like this. Ex:

````
1. blabla_variable = min(0, 1000)
2. print(blabla_variable)
############# Outputs ###############
0
````

This function ``min`` calculates the minimum of the numbers given as *arguments*. It is automatically imported without you having to do anything. To find some documentation about these functions that you don't have to import, you should type something like **minimum function python** in your browser and check on random websites that explain how to use it.

**Can I always call all functions like this ?**

Sadly.. No. Some functions are called only for specific things. For example, it would not make sense to use a function to *convert a text in lowercase* on a number (type ``int``).

So sometimes, functions are dependent on the *type* of one of the values that you want to modify with the function. To use these, we will write it as follows :

````
1. my_text = "HAHAHAHA I AM SO HAPPY"
2. print(my_text)

3. my_text2 = my_text.lower()
4. print(my_text2)
############# Outputs ###############
HAHAHAHA I AM SO HAPPY
hahahaha i am so happy
````

Here we used the function ``lower()`` which only works for texts (type ``str``) and letters (type ``char``). And because the functions are valid only for these 2 types, we write ``argument.function()`` instead of writing ``function(argument)``.

**Ok but I'm maybe a bit lost now...**

- No worries in a nutshell, we have **functions**.
- Functions are a **bunch of code** that can be called by its name to execute it.
- Functions can vary what they do with **arguments** given when you call them.
- Functions can give back something with the ``return`` special word at the end of them.
- Functions can sometimes only be executed for some **type of variables**. Then we write them ``argument.function()`` instead of ``function(argument)``.

Is it clear now ?
We'll see later on how functions are further used.

## Sequential types

It looks complicated but it isn't. *Sequential types* are types (such as ``int`` or ``str``) but that allow variables to have multiple values inside them (*sequences* of values).

Put otherwise, it's simply a *type* that allows a box (*variable*) to contain more than one *value*. Example:

````
# until now
variableA --> 1
variableB --> 'Hello'
variableC --> -6.90

# from now on also possible
variableD --> 1, 'Hello' and -6.90
````
(Note: this above is absolutely not code, I just wrote it in a code font.)

We are going to see 3 different sequential types:
- ``list``
- ``tuple``
- ``dict``

Right below!

## Lists

**What is a ``list``?**

Let us now see the first sequential type! This type is called a ``list``. It is used to store multiple things inside it.

A list can be created in 2 ways:
- ``my_little_list_variable = list()``: creates an empty list and stores it in the box ``my_little_list_variable``.
- ``my_other_list_variable = [1, 2, 3, 4, 1000]``: creates a list containing the integers 1, 2, 3, 4 and 1000. It stores the list in ``my_other_list_variable``.

So we just saw that elements in the list are one after another, and separated each time by a comma ``,``. The elements can be any type or value. Fo example,

````
1. aaaaaaa = list()
2. bbbbbbb = ['a', 'b', 'c', 'abracadabra']
3. ccccccc = [-9.99, 1000, True, '#FreeBritney', "Z"]

4. print(aaaaaaa)
5. print(bbbbbbb)
6. print(ccccccc)
############# Outputs ###############
[]
['a', 'b', 'c', 'abracadabra']
[-9.99, 1000, True, '#FreeBritney', "Z"]
````

Pretty straightforward until now, right ?

**But how can I use one element of a list?**

Right, the lists are no use if we can't access elements inside them. So to do so, you have to indicate the element's position. And the counting for the positions starts from the left with position ``0``. The positions are called *indices*, and each position is an *index*.

````
list -----> [-9.99, 1000, True, '#FreeBritney', "Z"]
indices --> [  0  ,  1  ,  2  ,       3       ,  4 ]
````

So to access the element ``True`` at position ``2``, I can write :
````
1. ccccccc[2]
2. # And then I can print it! (Remember? This line is a comment)
3. print(ccccccc[2])
############# Outputs ###############
True
````

**How can I access the last element of a very long list?**

It may be too complicated to count the indices of every position until the last one. So there exists a trick to start counting from the right ! However this time, positions start from ``-1`` and go down.

````
list -----> [-9.99, 1000, True, '#FreeBritney', "Z"]
indices --> [ -5  ,  -4 ,  -3 ,       -2      , -1 ]
````

Then you can use these the same way we used the normal ones.

````
1. print(ccccccc[-1])
2. print(ccccccc[-3])
############# Outputs ###############
Z
True
````

**How can I add elements to a list?**

Now we maybe want to add things to our list. You can add up 2 lists together by adding them with a ``+`` sign like this:

````
1. listA = [-9.99, 1000, True, '#FreeBritney', "Z"]
2. listB = [0.0]

3. listB = listA + listB

4. print(listA, listB)
############# Outputs ###############
[-9.99, 1000, True, '#FreeBritney', "Z"]
[-9.99, 1000, True, '#FreeBritney', "Z", 0.0]
````

Note: Here we stored the result of adding up ``listA`` and ``listB`` in the variable ``listB`` so that we don't have to create another variable. So this replaced the old value ``[0.0]`` with the result of ``listA + listB``.

**What else can I do with a list ?**

Good question! There are a bunch of *functions* that you can use on lists only (remember the functions that you can use on some types only). Here are some:

(Imagine we have a list such as ``list1 = [4, 3, 2, 1]``)

- ``list1.remove(a)``: Looks for and removes a from the list. Ex: ``list1.remove(2)`` gives back ``[4, 3, 1]``.
- ``list1.append(a)``: Adds the element ``a`` at the end of the list. Ex: ``list1.append(10000)`` gives back ``[4, 3, 2, 1, 10000]``.
- ``list1.insert(i, a)`` inserts the value ``a`` at position ``i`` in the list. Ex: ``list1.insert(1, "Hello")`` gives back ``[4, "Hello", 3, 2, 1]`` (remember that position 1 is the second when you start counting from the left, because we start from 0).
- ``list1.sort()``: reorders the list so that the elements are ranked (sorted) from smallest to largest. Ex: ``list1.sort()`` gives back ``[1, 2, 3, 4]``.

Again, to find some documentation about these functions or what other functions exist for ``list`` in python, just type **python list functions** (or similar) in your browser.

**I heard somewhere that lists are mutable. What does it mean?**

Good point. It means that you can modify elements inside them without creating a copy.

This means that you can access a single element and modify it and it will modify the list! Let us check this out with an example :

````
1. my_list1 = [-9.99, 1000, True, '#FreeBritney', "Z"]
2. print(my_list1)
3. print(my_list1[3])

4. my_list1[3] = 12
5. print(my_list1[3])
6. print(my_list1)
############# Outputs ###############
 [-9.99, 1000, True, '#FreeBritney', "Z"]
 #FreeBritney
 12
 [-9.99, 1000, True, 12, "Z"]
````

See? The element at index 3 has been replaced by 12 and thus it modified the list. We will see other types that don't allow this.

If you ask me I can explain to you how this can be a problem. But just remembering that you can modify element inside it is enough for now.

## Tuples

**What are tuples?**

Now lets see tuples. They also allow to store multiple things inside them. But instead of square brackets `[` they use parenthesis to distinguish them `(`.

````
1. my_tuple = (-9.99, 1000, True, '#FreeBritney', "Z")
2. print(my_tuple)
############# Outputs ###############
(-9.99, 1000, True, '#FreeBritney', "Z")
````

Similarly to lists, we can access elements with their indices.
````
1. print(my_tuple[2])
############# Outputs ###############
True
````

**What can tuples not do?**

``tuple`` doesn't have the functions that ``list`` has. So no ``remove``, ``append``, ``insert`` or ``sort``.

Sad.

**What can tuples do that list don't do then?**

They can be added together to create a new tuple. Like this :

````
1. tupleA = (1, 2, 3)
2. tupleB = ('a', 'b', 'c')

3. tupleC = tupleA + tupleB
4. print(tupleC)
############# Outputs ###############
(1, 2, 3, 'a', 'b', 'c')
````

They can be augmented like this:

````
1. tupleA = (1, 2, 3)

3. tupleC = tupleA * 5
4. print(tupleC)
############# Outputs ###############
(1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3)
````

**And so are tuples mutable?**

No! They're *immutable*. So it means that yo cannot modify an element inside them.

````
1. tupleA = (1, 2, 3)
2. print( tupleA[0] )

3. tupleA[0] = 10
############# Outputs ###############
1
!!! Error with a lot of complicated stuff but should be saying you're not allowed to do this!!!
````

If you ask me when to use ``tuple`` or ``list``, I would say use ``list`` and if you cannot do something that you want to do, try ``tuple``. But ``list`` is better.



© Nicolas d'Argenlieu, all rights reserved.
