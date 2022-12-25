# Day 6: Functions, built-in functions, a function definition, indentation, spaces vs tabs, _while_ loop, infinite loop.

> ## Day topics:
>
>1.1. **Functions**, **built-in** functions, a function definition.  
>1.2. Indentation, spaces vs tabs.  
>1.3. _While_ loop, infinite loop.  
>1.4. **Day project:** "Maze". 

### 1.1. Functions, built-in functions, a function definition.

> #### _Functions are "self contained" modules of code that accomplish a specific task._

Functions usually "take in" data, process it, and "return" a result. Once a function is written, it can be used over and over and over again.  
Functions can be "called" from the inside of other functions.

<img src="https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/function_def.png" width=70% height=70%>

#### Why do we Write Functions?

- Functions allow us to conceive of our program as a bunch of sub-steps.  
- Functions allow us to reuse code instead of rewriting it.  
- Functions allow us to test small parts of our program in isolation from the rest.

_**Syntax:**_

```python
def function_name():
    # first step
    # second step
    # ...
```

_**Example 1:**_

```python
def my_function():
  print("Hello")

my_function()
```

_**Example 2:**_

```python
def add_num(num_1, num_2):
    print(num_1 + num_2)

add_num(5, 2)  # Output: 7
```

#### Python built-in functions.

> #### _A built-in function is a function that is already available in a programming language, application, or another tool that can be accessed by end users._

## [ALL PYTHON BUILT-IN FUNCTIONS YOU CAN FIND HERE](https://docs.python.org/3/library/functions.html)

![built-in functions](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/built_in_functions.png)

### 1.2. Indentation, spaces vs tabs.

> #### _Indentation refers to the spaces at the beginning of a code line._

Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important.  
Python uses indentation to indicate a block of code.

_**Example 1:**_

```python
if 7 > 3:
    print("The number is still greater then '3'.")
```

_**Example 2: syntaxis error**_

```python
if 7 > 3:
print("The number is still greater then '3'.")  
# Python will give an error.
```
#### Python built-in functions.

> #### _Spaces are the preferred indentation method according by "PEP 8 – Style Guide for Python Code"._

Tabs should be used solely to remain consistent with code that is already indented with tabs.  
Python disallows mixing tabs and spaces for indentation.

## [CHECK A VIDEO 'TABS VS SPACES'](https://www.youtube.com/watch?v=SsoOG6ZeyUI&ab_channel=ChristianNyffenegger)


Also I found another opinion: 

_"Well well, seems like everybody is strongly biased towards spaces. I use tabs exclusively.I know very well why._ 

_Tabs are actually a cool invention, that came after spaces. It allows you to indent without pushing space millions of times or using a fake tab (that produces spaces)._  

_I really don't get why everybody is discriminating the use of tabs. It is very much like old people discriminating younger people for choosing a newer more efficient technology and  
complaining that pulse dialing works on every phone, not just on these fancy new ones. "Tone dialing doesn't work on every phone, that's why it is wrong"._

_Your editor cannot handle tabs properly? Well, get a modern editor. Might be darn time, we are now in the 21st century and the time when an editor was a high tech complicated piece of software is long past.  
We have now tons and tons of editors to choose from, all of them that support tabs just fine. Also, you can define how much a tab should be, a thing that you cannot do with spaces.  
Cannot see tabs? What is that for an argument? Well, you cannot see spaces neither!_

_May I be so bold to suggest to get a better editor? One of these high tech ones, that were released some 10 years ago already, that display invisible characters? (sarcasm off)._

_Using spaces causes a lot more deleting and formatting work. That is why (and all other people that know this and agree with me) use tabs for Python._

_Mixing tabs and spaces is a no-no and no argument about that. That is a mess and can never work."_

### 1.3. While loop, infinite loop.

> #### _The while loop is a control flow statement that allows code to be executed repeatedly based on a given Boolean condition._

_**Syntax:**_

```python
while condition is True:
    execute the code in the loop's body
```

<img src="https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/while_loop_diagram.jpg" width=50% height=50%>

_**Example 1:**_

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

 _**Example 2:**_

```python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

#### Infinite loop.

> #### _An infinite loop (or endless loop) is a sequence of instructions that, as written, will continue endlessly, unless an external intervention occurs ("pull the plug")._

_**Example 1:**_

```python
i = 1
while i < 6:
    print(i)  
# 'i' is always less then 6 so the print function will executs endlessly.
```

#### When are Infinite Loops Necessary?

- An infinite loop may be useful in client/server programming where the server needs to run with continuity so that the client programs may communicate with the server program whenever the necessity arises.  
- It may also be helpful if a new connection needs to be created.  
- There is the utility of a while loop in a gaming application or an application where we enter some sort of main event loop, which continues to run until the user selects an action to break that infinite loop.  
- Also, if one has to play a game and wishes the game to reset after each session. Iterations are the process of doing a repetitive task, and computer programs have always mastered this art.


### 1.4. Day project: "Maze".

Write a program using an if/elif/else statement so Reeborg can find the exit.  
The secret is to have Reeborg follow along the right edge of the maze, turning right if it can,  
going straight ahead if it can’t turn right, or turning left as a last resort.

## [FIND THE GAME HERE](https://reeborg.ca/reeborg.html?lang=en&mode=python&menu=worlds%2Fmenus%2Freeborg_intro_en.json&name=Maze&url=worlds%2Ftutorial_en%2Fmaze1.json)

_**Solution:**_

```python
def turn_right():
    turn_left()
    turn_left()
    turn_left()
def jump():
    turn_right()
    move()
    turn_right()
    
while front_is_clear():
    move()
turn_left()

while not at_goal():
    if not front_is_clear() and right_is_clear():
        turn_right()
    elif front_is_clear() and right_is_clear():
        turn_right()
    elif not front_is_clear() and not right_is_clear():
        turn_left()
        while not front_is_clear():
            turn_left()
    move()
```

---

### Resources:

<https://www.cs.utah.edu/~germain/PPS/Topics/functions.html>  
<https://dev.to/navi/why-functional-programming-matters-2o95>  
<https://docs.python.org/3/library/functions.html>  
<https://www.w3schools.com/python/python_while_loops.asp>  
<https://www.w3schools.com/python/python_while_loops.asp>
<https://stackoverflow.com/questions/120926/why-does-python-pep-8-strongly-recommend-spaces-over-tabs-for-indentation> 
<https://www.educba.com/python-infinite-loop/>  

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[DAY 5 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%205.md)
