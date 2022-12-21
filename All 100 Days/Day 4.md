# Day 4: Module, import, random modul, randint(), random(), choice(), list, list elements, len(), index(), append(), extend(), nested list.

> ## Day topics:
>
>1.1. **Module**, **Import**.  
>1.2. **Random module**, **randint()**, **random()** and **choice()**.  
>1.3. **List** definition.  
>1.4. List elements **extraction**, **len()** and **index()**.    
>1.5. **Append()** method.  
>1.6. **Extend()** method.   
>1.7. **Nested list**.   
>1.8. **Day project:** "Hide the treasure" and "Rock, Paper, Scissors".  

### 1.1. Module, Import.

> #### _The Module is a file with a script of a program (code) which was written for the purpose of using it in the future instead of rewriting it again._

The file name is the module name with the suffix .py appended. A module can contain executable statements as well as function definitions. These statements are intended to initialize the module.  
They are executed only the first time the module name is encountered in an import statement.  

> #### _The process by which Python code in one module is made available to Python code in another module._

When an import statement is executed, the standard builtin __import__() function is called. 

_**Example 1:** When the import is used, it searches for the module initially in the local scope by calling __import__() function. The value returned by the function is then reflected in the output of the initial code._

```python
import math
pie = math.pi
print("The value of pi is : ", pie)
```

_**Example 2:** In the above code module, math is imported, and its variables can be accessed by considering it to be a class and pi as its object. 
The value of pi is returned by __import__(). pi as a whole can be imported into our initial code, rather than importing the whole module._

```python
from math import pi
 
# Note that in the above example,
# we used math.pi. Here we have used
# pi directly.
print(pi)
```

### 1.2. Random module, randint(), random() and choise().

> #### _The Random module is a Python built-in module that implements pseudo-random number generators for various distributions._

The random module has a set of methods, some of them are:

- randind()
- random()
- choice()

> #### _The Random() method returns a random float number between 0 and 1._

_**Example:**_

```python
import random

print(random.random())
```

> #### _The Randind() method returns number between the given range._

_**Example:**_

```python
import random

print(random.randint(1, 9))
```

> #### _The Choice() method returns a random element from the given sequence._

_**Example:**_

```python
import random

fruits = ["apple", "banana", "cherry"]
print(random.choice(fruits))
```

_**Coding exercise 1:**  
You are going to write a program that will select a random name from a list of names. The person selected will have to pay for everybody's food bill.
You are going to write a virtual coin toss program. It will randomly tell the user "Heads" or "Tails"._

_**Solution:**_

```python
names_string = input("Give me everybody's names, separated by a comma. ")
import random
result = random.randint(0, 1)
if result == 1:
    print("Heads")
else:
    print("Tails")
```

_**Coding exercise 2:**  
You are going to write a program that will select a random name from a list of names. The person selected will have to pay for everybody's food bill.
Important: You are not allowed to use the choice() function._

_**Solution:**_

```python
names_string = input("Give me everybody's names, separated by a comma. ")
names_list = names_string.split(", ")
people_count = len(names_list)
import random
bill_payer_number = random.randint(0, people_count -1)
bill_payer_name = names_list[bill_payer_number]
print(f"{bill_payer_name} is going to buy the meal today!")
```

### 1.3. List definition.

> #### _A list is a data structure in Python that is a mutable, or changeable, ordered sequence of elements. Each element or value that is inside of a list is called an item._

Lists are used to store multiple items in a single variable.

_**Syntax:**_

```python
my_list = ['element 1', 'element 2', 'element 3', 'element 4']
```

_**Example 1:**_

```python
my_list = [1, 3, 5, 2, 4]
print(my_list)  # Returns [1, 3, 5, 2, 4]
```

_**Example 2:**_

```python
cities = ["Montevideo", "Toronto", "Helsinki", "Bangkok"]
print(cities)  # Returns ["Montevideo", "Toronto", "Helsinki", "Bangkok"]
```

### 1.4. List elements extraction, len() and index().

> #### _List elements extraction is made by [ ]._

_**Syntax:**_

```python
my_list_name[index of element]
```
_**Example:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(list_1[0])  # Returns 'window'
print(list_1[1])  # Returns 'door'
print(list_1[2])  # Returns 'lamp'
print(list_1[3])  # Returns 'table'
```

> #### _The len() function returns the number of items in a list._

_**Syntax:**_

```python
len(object)
```

_**Example:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(f'Number of items in the list is: {len(list_1)}')
# Returns 'Number of items in the list is: 4'
```

> #### _The index() function searches a given element from the start of the list and returns the index of the first occurrence._

In Python, each item in a list is associated with a number. The number is known as a list index.

_**Syntax:**_

```python
list_name.index(element, start)
```

_**Example 1:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(list_1.index('door', 0))  # Returns '1'
```

The ordinal number (index) of the first element is '0'.  
The ordinal number (index) of the second element is '1' and so on.

_**Example 1:**_

```python
list_1 = ['window', 'door', 'lamp', 'table', 'window']
print(list_1.index('window', 0))  # Returns '0'
print(list_1.index('door', 0))  # Returns '1'
print(list_1.index('lamp', 0))  # Returns '2'
print(list_1.index('table', 0))  # Returns '3'
print(list_1.index('window', 2))  # Returns '4'
```
_**Example 2:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(f'Number of items in the list is: {len(list_1)}')
# Returns 'Number of items in the list is: 4'
# BUT!
print(f'The index of the first element is: {list_1.index("window",0)}')
# The index of the first element 'window' is '0'
print(f'The index of the last element is: {list_1.index("table",0)}')
# The index of the last element 'table' is '3'
# AND! If element does not exist.
print(list_1.index('door', 2))  # Returns 'ValueError: 'door' is not in list'
```

#### Changing elements in a list.

_**Syntax:**_

```python
list_name[index of element] = 'new element'
```

_**Example 1:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
list_1[0] = 'book'
print(list_1)
# Returns ['book', 'door', 'lamp', 'table']
```

### 1.5. Append() method.  

> #### _The Append() method appends an element to the end of the list._

Length of the list increases by 1

_**Syntax:**_

```python
list.append(element)
```

_**Example 1:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(list_1)
# Returns ''window', 'door', 'lamp', 'table']
# Add element 'cat'.
list_1.append('cat')
print(list_1)
# Returns ''window', 'door', 'lamp', 'table', 'cat']
```

### 1.6. Extend() method.  

> #### _The Append() method appends a number of elements to the end of the list._

	Length of the list increases by the number of elements in the iterable.

_**Example:**_

```python
list_1 = ['window', 'door', 'lamp', 'table']
print(list_1)
# Returns ''window', 'door', 'lamp', 'table']
# Add elements 'cat', 'moon', 'sea'.
list_1.extend(['cat', 'moon', 'sea'])
print(list_1)
# Returns ''window', 'door', 'lamp', 'table', 'cat', 'moon', 'sea']
```

### 1.7. Nested list.

> #### _A nested list in Python allows a list to contain multiple sublists within itself._

Each sublist can have items of different data types. It can be created by placing comma-separated sublists and items together.  

_**Example:**_

```python
L = ['a', ['bb', ['ccc', 'ddd'], 'ee', 'ff'], 'g', 'h']
```

![Nested list](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/nested_list.png)

#### Create a nested list. 

_**Solution 1:**_

```python
ist_1 = [1, 2, 3, 4]
list_2 = ['one', 'two', 'three']
list_3 = []
list_3.append(list_1)
list_3.append(list_2)
print(list_3)  # Returns [[1, 2, 3, 4], ['one', 'two', 'three']]
```

_**Solution 2:**_

```python
list_1 = [1, 2, 3, 4]
list_2 = ['one', 'two', 'three']
list_3 = [list_1, list_2]
print(list_3)  # Returns [[1, 2, 3, 4], ['one', 'two', 'three']]
```

_**Exsemple:**_

```python
fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"]
vegetables = ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]
food = [fruits, vegetables]
print(food[0][0])  # Returns 'Strawberries'.
print(food[0][1])  # Returns 'Nectarines'.
print(food[1][0])  # Returns 'Spinach'.
print(food[1][1])  # Returns 'Kale'.
```

## 1.7. Day project.

#### Bootcamp day project 1: "Hide the treasure".

You are going to write a program that will mark a spot with an X.  
In the starting code, you will find a variable called map.  
This map contains a nested list.

_**Solution:**_

```python
# Don't change the code below
row1 = ["⬜️","️⬜️","️⬜️"]
row2 = ["⬜️","⬜️","️⬜️"]
row3 = ["⬜️️","⬜️️","⬜️️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")

#Write your code below this row
column = int(position[0])
row = int(position[1])
map[row - 1][column - 1] = 'X'

# Don't change the code below
print(f"{row1}\n{row2}\n{row3}")
```

#### Bootcamp day project 2: "Rock, Paper, Scissors".

Make a rock, paper, scissors game.  
You'll find the ASCII art for the hand signals already saved to a corresponding variable: rock, paper, and scissors.  
Start the game by asking the player: "What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors."  
You can find the "official" rules of the game on the [World Rock Paper Scissors Association website](https://wrpsa.com/the-official-rules-of-rock-paper-scissors/).

```python
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
# Write your code below this line
import random

gamer_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))
list_of_options = [rock, paper, scissors]
comp_choice = random.randint(0, 2)
if gamer_choice == 0 and comp_choice == 1:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You lose!")
elif gamer_choice == 0 and comp_choice == 2:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You win!")
elif gamer_choice == 1 and comp_choice == 0:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You win!")
elif gamer_choice == 1 and comp_choice == 2:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You lose!")
elif gamer_choice == 2 and comp_choice == 0:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You lose!")
elif gamer_choice == 2 and comp_choice == 1:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("You win!")
else:
    print(list_of_options[gamer_choice])
    print(list_of_options[comp_choice])
    print("Try again!")
```

---

### Resources:

<https://docs.python.org/3/tutorial/modules.html>  
<https://docs.python.org/3/reference/import.html>  
<https://www.geeksforgeeks.org/import-module-python/>  
<https://docs.python.org/3/library/random.html>  
<https://www.educative.io/answers/what-is-a-python-list>  
<https://www.geeksforgeeks.org/python-list-index/>  
<https://developers.google.com/edu/python/lists>  
<https://www.w3schools.com/python/ref_list_append.asp>  
<https://www.geeksforgeeks.org/difference-between-append-extend-and-insert-in-python/>  
<https://www.learnbyexample.org/python-nested-list/>  


---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[DAY 3 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%203.md)
