# Day 3: Conditional statements: if, elif, else; Comparison operators: >, <, >=, <=, ==, !=; Modulo %; Logical operators: and, or, not; Lower(); Count(); Day projects: Treasure Island, S????

> ## Day topics:
>
>[1.1. **Conditional statements:** if, elif, else](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%203.md#11-conditional-statments-if-elif-else)    
>[1.2. **Comparison operators:** >, <, >=, <=, ==, !=](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#12-comparison-operators)  
>[1.3. **Modulo %** ](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#13-modulo-)  
>[1.4. **Logical operators:** and, or, not](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#14-logical-operators-and-or-not)  
>[1.5. **Lower()** method](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#15-lower-function)  
>[1.6. **Count()** method](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#16-count-function)  
>[1.7. **Day projects:** Treasure Island, Service price calculator](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#17-day-projects)  

### 1.1. Conditional statments: if, elif, else

> #### _Conditional Statement in Python perform different computations or actions depending on whether a specific Boolean constraint evaluates to true or false._

Python has 3 key Conditional statements:

- if statement
- if-else statement
- if-elif-else ladder  

>####  _if statement_ is used for decision-making operations. It contains a body of code which runs only when the condition given in the if statement is true. 

These statements guide the program while making decisions based on the conditions encountered by the program.

![if statement flowchart](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/if%20statement.png)

_**Example:**_
 
```python
number = 5
# Check if number is greater than 0
if number > 0:
    print("Number is positive.")
# The next line of code executes even though "if statement" is False
name = "John"
print(name)
```

>#### _if-else statement_ is used when you have to judge one statement on the basis of other. If one condition goes wrong, then there should be another condition that should justify the statement or logic.

_**Example:**_

```python
number = 7
if number > 0:
    print("Positive number")
else:
    print("Negative number")
```

>#### _if-elif-else statement_ is used when the first if statement isn't true, but you want to check for another condition. Meaning, if statements pair up with elif and else statements to perform a series of checks.

_**Example:**_

```python
number = 7
number = 0
if number > 0:
    print("Positive number")
elif number == 0:
    print('Zero')
else:
    print('Negative number')
```

>#### _Nested if statments:_ You can have if statements inside if statements

```python
number = 80
if number > 10:
    print("Number is above 10.")
    if number > 20:
        print("And also above 20.")
    else:
        print("But not above 20.")
```

### 1.2. Comparison operators: >, <, >=, <=, ==, !=

> #### _Comparison operators are used to compare two values._

- **Greater than** (>) 
- **Less than** (<) 
- **Greater than or equal to** (>=)
- **Less than or equal to** (<=)
- **Equal** (==)
- **Not equal** (!=)

_**Example 1:**_

```python
num_1 = 5
num_2 = 2
print(num_1 > num_2)  # Returns True
```

_**Example 2:**_

```python
num_1 = 1
num_2 = 5
print(num_1 < num_2)  # Returns True
print(num_1 > num_2)  # Returns False
```

_**Example 3:**_

```python
num_1 = 1
num_2 = 5
num_3 = 7
print(num_1 <= num_2)  # Returns True
print(num_3 >= num_2)  # Returns True
print(num_1 >= num_1)  # Returns True
```

_**Example 4:**_

```python
num_1 = 1
num_2 = 5
print(num_1 == num_2)  # Returns False
print(num_1 != num_2)  # Returns True
```

_**Exercise:** write a program which counts days, weeks and months remaining to your 100 years anniversary._

```python
age = input("What is your current age? ")
age_as_int = int(age)
years_remaining = 100 - age_as_int
days = years_remaining * 365
weeks = years_remaining * 52
months = years_remaining * 12
result = f"You have {days} days, {weeks} weeks, and {months} months left."
print(result)
```

### 1.3. Modulo %  

> #### Modulo % returns the remainder of dividing the left hand operand by right hand operand._

It's used to get the remainder of a division problem.

```python
num_1 = 10
num_2 = 5
num_3 = 3
print(num_1 % num_2)  # Returns '0'
print(num_1 % num_3)  # Returns '1'
```

```python
num_1 = 10
num_1 = 100
num_2 = 30
print(num_1 % num_2)  # Returns '10'.
# 100 % 30 = (30 +30 +30) + and 10, where '10' is the remainder.
```

_**Exercise:**  
Write a program that works out whether if a given number is an odd or even number. Given number should be an integer._

_**Solution:**_

```python
number = int(input("Which number do you want to check?\n"))
if number % 2 == 0:
    print("This is an even number.")
else:
    print("This is an odd number.")
```

### 1.4. Logical operators: and, or, Nnot

> #### _Logical operators are used on conditional statements (either True or False). They perform Logical AND, Logical OR and Logical NOT operations._
  
- **and**: True if both the operands are true
- **or**:  True if either of the operands is true	
- **not**: True if operand is false

_**Example 1:**_

```python
a = 10
b = 10
if a > 0 and b > 0:
    print("True")  # Returns True
else:
    print("False")
```

_**Example 2:**_

```python
a = 10
b = 10
if a > 0 or b > 0:
    print("True")  # Returns True
else:
    print("False")
```

_**Example 3:**_

```python
a = 10
if not a > 0:
    print("True")
else:
    print("False")  # Returns False
```

_**Exercise:**  
Write a program that interprets the Body Mass Index (BMI) based on a user's weight and height.  
The BMI is calculated by dividing a person's weight (in kg) by the square of their height (in m).  
It should tell them the interpretation of their BMI based on the BMI value.  
Under 18.5 they are underweight. Over 18.5 but below 25 they have a normal weight.  
Over 25 but below 30 they are slightly overweight. Over 30 but below 35 they are obese.  
Above 35 they are clinically obese._

_**Solution:**_

```python
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
bmi = weight / height ** 2
bmi_rounded = round(bmi)
if bmi < 18.5:
    print(f"Your BMI is {bmi_rounded}, you are underweight.")
elif bmi < 25:
    print(f"Your BMI is {bmi_rounded}, you have a normal weight.")
elif bmi < 30:
    print(f"Your BMI is {bmi_rounded}, you are slightly overweight.")
elif bmi < 35:
    print(f"Your BMI is {bmi_rounded}, you are obese.")
else:
    print(f"Your BMI is {bmi_rounded}, you are clinically obese.")
```

_**Exercise:**  
Write a program that works out, whether a given year is a leap year. A normal year has 365 days, and leap years have 366, with an extra day in February.
This is how you find out: leap year is every year that is evenly divisible by 4, except every year that is evenly divisible by 100, unless the year is also evenly divisible by 400._

_**Solution:**_

```python
year = int(input("Which year do you want to check? "))
if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print("Leap year.")     
        else:
            print("Not leap year.")
    else:
        print("Leap year.")        
else:
    print("Not leap year.")
```

### 1.5. Lower() method

> #### _Lower() method takes no arguments and returns the lowercased strings from the given string by converting each uppercase character to lowercase._

If there are no uppercase characters in the given string, it returns the original string.

_**Example 1:**_

```python
message = "PYTHON"
message = message.lower()
print(message)  # Output: python 
```
_**Example 2:**_

```python
message = "PYTHON"
print(message.lower())  # Output: python 
```

### 1.6. Count() method

> #### _The count() method returns the number of occurrences of a substring in the given string._


_**Example 1:**_

```python
message = "python is programming language"
# Find a number of occurrence of 'p'
number = message.count('p')
print("Number of occurrence of p:", number)  # Output: Number of occurrence of p: 2
```

_**Example 2:**_

```python
message = "python is programming language"
# Find a number of occurrence of 'p'
print("Number of occurrence of p:", message.count('p'))  # Output: Number of occurrence of p: 2
```

### 1.7. Day projects

#### Bootcamp day project: Treasure Island

```python
# If the bill was $150.00, split between 5 people, with 12% tip. 
# Each person should pay (150.00 / 5) * 1.12 = 33.6
# Format the result to 2 decimal places = 33.60
# Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.

print("Welcom to the tip calculator.")
bill = float(input("What was the total bill? $"))
tip_persentage = int(input("What persentage tip would you lake to give? 10, 12 or 15? "))
number_of_people = int(input("How many people to split the bill? "))
tip_sum = tip_persentage * bill / 100
pay_sum = bill + tip_sum / number_of_people
sum_for_each = round((pay_sum / number_of_people),2)
print(f"Each person should pay: ${sum_for_each}")
````

#### My day project: Service price calculator

```python
# The calculator calculates the cost of the service based on the input data.
# It is assumed that the apartment always has at least 1 window and a door. No zero values are used.

print("Calculate the price for our service.")
square = float(input("How many sq.meters in your apartment: "))
windows = int(input("How many windows in your apartment: "))
doors = int(input("How many doors in your apartment: "))
pets = int(input("Do you have pets in the apartment? If no type in '0', if you have type in '1': "))
price_base = 15

# Calculating a cost based on the input and multiplying on indexes if applicable
price_on_square = price_base * square
price_on_windows = price_base * windows * 1.4
price_on_doors = price_base * doors * 1.2
price_on_pets = price_base * pets * 20
price = round((price_on_square + price_on_windows + price_on_doors + price_on_pets), 2)

# Calculating a cost based on the start date of the service
price_urgent = round((price * 1.3), 2)
print(f"Total price for cleaning service is:\nWe start tomorrow or later: ${price}\nWe start today: ${price_urgent}")
print("Call us now and get 10% discount!")

````

---

### Resources:

<https://www.naukri.com/learning/articles/conditional-statement-in-python/>  
<https://www.guru99.com/if-loop-python-conditional-structures.html>  
<https://www.programiz.com/python-programming/if-elif-else>  
<https://www.idtech.com/blog/what-does-elif-mean-in-python#>  
<https://www.w3schools.com/python/gloss_python_comparison_operators.asp>  
<https://www.geeksforgeeks.org/python-logical-operators-with-examples-improvement-needed/>  
<https://www.programiz.com/python-programming/methods/string/lower>  
<https://www.programiz.com/python-programming/methods/string/count>  








 

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[TO THE DAY 1 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%201.md)
