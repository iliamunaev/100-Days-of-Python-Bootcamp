# Day 5: loop, _for_ loop, range().

> ## Day topics:
>
>1.1. **Loop** definition,  **for** loop.  
>1.2. **Range()** function.  
>1.3. **Day project:** "Password Generator". 

### 1.1. Loop definition, _for_ loop.

> #### _The loop is a sequence of instruction s that is continually repeated until a certain condition is reached._

> #### _The for loops are used when you have a block of code which you want to repeat a fixed number of times._
The Python _for_ statement iterates over the members of a sequence in order, executing the block each time. 

_**Example 1:**_

```python
for x in range(0, 3):
    print("Hello!")
```

_**Example 2:**_

```python
my_list = ["car", "ship", "plane"]
for vehicle in my_list:
    print(vehicle)
```

_**Example 3:**_

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
    print(x)
```

_**Coding exercise 1:**_   
_You are going to write a program that calculates the average student height from a List of heights.
Important You should not use the sum() or len() functions in your answer._

_**Solution:**_

```python
# Don't change the code below
student_heights = input("Input a list of student heights ").split()
for n in range(0, len(student_heights)):
    student_heights[n] = int(student_heights[n])

# Write your code below this row
sum_heights = 0
total_num_students = 0
for n in student_heights:
    sum_heights += n
    total_num_students += 1
avg_height = round(sum_heights / total_num_students)
print(avg_height)
```

_**Coding exercise 2:**_  
_You are going to write a program that calculates the highest score from a List of scores.
Important you are not allowed to use the max() or min() functions._

_**Solution:**_

```python
# Don't change the code below
student_scores = input("Input a list of student scores ").split()
for n in range(0, len(student_scores)):
    student_scores[n] = int(student_scores[n])
print(student_scores)

# Write your code below this row
highest_score = 0
for n in student_scores:
    if highest_score < n:
        highest_score = n
print(f"The highest score in the class is: {highest_score}")
```

### 1.2. Range() function.

> #### _The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number._

_**Syntax:**_

```python
lrange(start, stop, step)
```
Parameter values:
- _Start_ is optional. An integer number specifying at which position to start. Default is 0.
- _Stop_ if required. An integer number specifying at which position to stop (not included).
- _Step_ is optional. An integer number specifying the incrementation. Default is 1.

_**Example 1:**_

```python
x = range(1, 6)  # Start from '1', stop before '6', '6' is not included, step is '1'.
for n in x:
    print(n)
```

_**Example 2:**_

```python
x = range(2, 40, 3)  # Start from '2', stop before '40', '40' is not included, step is '3'.
for n in x:
    print(n)
```

_**Coding exercise 1:**_  
_You are going to write a program that calculates the sum of all the even numbers from 1 to 100._

_**Solution 1:**_

```python
total = 0
for n in range(2, 101, 2):
    total += n
print(total)
```

_**Solution 2:**_

```python
total = 0
for n in range(1, 101):
    if n % 2 == 0:
        total += n
print(total)
```

_**Coding exercise 2:**_  
_You are going to write a program that automatically prints the solution to the FizzBuzz game.  
Your program should print each number from 1 to 100 in turn.  
When the number is divisible by 3 then instead of printing the number, it should print "Fizz".  
When the number is divisible by 5, then instead of printing the number, it should print "Buzz".  
And if the number is divisible by both 3 and 5 e.g. 15, then instead of the number, it should print "FizzBuzz"._

_**Solution 1:**_

```python
shout = 1
for n in range(1, 101):
    if shout % 3 == 0 and not shout % 5 == 0:
        print("Fizz")
        shout += 1
    elif shout % 5 == 0 and not shout % 3 == 0:
        print("Buzz")
        shout += 1
    elif shout % 3 == 0 and shout % 5 == 0:
        print("FizzBuzz")
        shout += 1
    else:
        print(shout)
        shout += 1
```

_**Solution 2:**_

```python
for n in range(1, 101):
    if n % 3 == 0 and n % 5 == 0:
        print("FizzBuzz")
    elif n % 3 == 0:
        print("Fizz")
    elif n % 5 == 0:
        print("Buzz")
    else:
        print(n)
```

## 1.3. Day project.

#### Bootcamp day project: "Password Generator".

The objective is to take the inputs from the user to these questions and then generate a random password.  
Use your knowledge about Python lists and loops to complete the challenge.  

**Easy Version** (Step 1): Generate the password in sequence.  
If the user wants 4 letters, 2 symbols and 3 numbers then the password might look like this: fgdx$(924  
You can see that all the letters are together. All the symbols are together and all the numbers follow each other as well.

**Hard Version** (Step 2): In the advanced version of this project the final password does not follow a pattern.  
So the example above might look like this: x$d24g(f9  
And every time you generate a password, the positions of the symbols, numbers, and letters are different.

_**Solution:**_

```python
import random

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v',
           'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R',
           'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters = int(input(f"How many letters would you like in your password?\n"))
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))
password_list = []
for n in range(nr_letters):
    password_list.append(random.choice(letters))
for s in range(nr_symbols):
    password_list.append(random.choice(symbols))
for c in range(nr_numbers):
    password_list.append(random.choice(numbers))

random.shuffle(password_list)
password = ""
for p in password_list:
    password += p
print(password)
```

---

### Resources:

<https://www.techtarget.com/whatis/definition/loop>  
<https://wiki.python.org/moin/ForLoop>  
<https://www.w3schools.com/python/ref_func_range.asp>  


---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[DAY 4 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%204.md)
