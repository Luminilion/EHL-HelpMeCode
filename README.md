# Cheatsheet Python EHL
A l’attention de Mlle A.C.

## Basics that he did not include

<span style="color:red">What is code?</span> <br>
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

<span style="color:red">What is a variable?</span> <br>
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

<span style="color:red">What are types?</span> <br>
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

<span style="color:red">What is a package?</span> <br>
A package is a bunch of files containing code written by someone else. You can re-use the code by *importing* it in your own code. Example: *statistics* package contains everything related to statistical computations. It spares you from re-writing the calculations for an average, a standard deviation…

*Metaphor:* See a package as a gardener. He contains a lot of knowledge about plants. If you want to grow plants, you can either ask him to explain to you precisely how to grow plants. Or you can just tell him to grow plants in your garden. The first thing implies you have to redo everything he tells you. The second implies that you just tell him what you want to grow and he'll do it. <br> Well the first case is writing all the code by yourself and the second case is just using a package and telling the package to do some specific things (e.g. grow a plant).

<span style="color:red">How to use a package?</span> <br>
You must import it into your code (otherwise your code does not know where all the knowledge is). There are multiple ways:

```
1.  import statistics
2.  from statistics import average
3.  import statistics as st
```

- ``1.`` simply imports the package called ``statistics``. This means that you can use the code from the package in your code.
- ``2.`` imports only the bunch of code called ``average`` from the package ``statistics``.
- ``3.`` imports the package called ``statistics`` but gives it a little name ``st`` so that in your code you can simply write ``st`` and not statistics every time you want to use a bunch of code from the package.

<span style="color:red">What is a comment?</span><br>
A comment is a bunch of code that is not going to be executed by the computer. It is here if you want to write explanations in english (or french or whatever) in the middle of your code. Everything on the right of the `#` on the same line will not be executed.
```
1. blabla() # This code launches a nuclear war
2. blabla2() # This code does a great drawing
```

<span style="color:red">What is indentation?</span> <br>
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

<span style="color:red">What is ``if __name__ == '__main__'``?</span><br>
Forget about this, it's useless for you and implies complicated stuff. Ask me if you really want to understand.

## `if` statements

<span style='color:red'> What is `if`?</span>
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

<span style="color:red">What if I want to do something else if `conditionA` is not true?</span>

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

<span style="color:red">How can I do different things for different conditions? </span>

You mean that you want to do something if `conditionA` is True, but something else if `conditionB` is True and something else if both are false ?

Ok let us do this using the word `elif`. This word is a mix between `else` and `if`. It means "if the previous condition is false, try me! But I have a condition as well". Ex:

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
- And arrive to line `5.`, where there is another ``conditionB``. This one is ``True``! So the computer enters the elif.
- The computer executes line `6.` and continues.
- Line `7.` is skipped because one of the previous conditions was verified.
- Line `8.` is skipped because line `7.` on which it depends is skipped.
- Line `9.` always executes because it's independent!

Note1: this kind of multiple choice always starts with `if`.

Note2: There can only be one `if` or `elif` or `else` that is entered by the computer. Once it is done all the following are skipped even if the conditions are `True`.

Note3: Consider the `else` as the trash. If no condition is `True`, well the computer always ends up entering the `else`.

<span style="color:red">How can I do more complicated conditions ?</span> <br>

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



NDA Copyright :)
