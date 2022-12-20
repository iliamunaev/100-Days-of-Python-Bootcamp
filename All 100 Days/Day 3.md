# Day 3: Conditional statements: if, elif, else; Comparison operators: >, <, >=, <=, ==, !=; Modulo %; Logical operators: and, or, not; Lower(); Count(); Day projects: Treasure Island, S????

> ## Day topics:
>
>[1.1. **Conditional statements:** if, elif, else](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%203.md#11-conditional-statments-if-elif-else)    
>[1.2. **Comparison operators:** >, <, >=, <=, ==, !=](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#12-comparison-operators)  
>[1.3. **Modulo %** ](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#13-modulo-)  
>[1.4. **Logical operators:** and, or, not](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#14-logical-operators-and-or-not)  
>[1.5. **Lower()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#15-lower-function)  
>[1.6. **Count()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%203.md#16-count-function)  
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

>####  _if-else statement_ is used when you have to judge one statement on the basis of other. If one condition goes wrong, then there should be another condition that should justify the statement or logic.

_**Example:**_

```python
number = 7
if number > 0:
    print("Positive number")
else:
    print("Negative number")
```

>####  _if-elif-else statement_ is used when the first if statement isn't true, but you want to check for another condition. Meaning, if statements pair up with elif and else statements to perform a series of checks.

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

>####  _Nested if statments:_ You can have if statements inside if statements

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

#### Exercise

Find a sum of two numbers, which the user type in the request

_**Solution 1:**_

```python
two_digit_number = input("Type a two digit number: ")
char_1 = two_digit_number[0]  # Pull out character number 1
char_2 = two_digit_number[1]  # Pull out character number 2
char_1_int = int(char_1)  # Convert character 1 from string to integer class
char_2_int = int(char_2)  # Convert character 2 from string to integer class
result = char_1_int + char_2_int
print(result)
```

_**Solution 2:**_

```python
two_digit_number = input("Type a two digit number: ")
char_1 = int(two_digit_number[0])   # Pull out and convert character number 1 from string to integer class
char_2 = int(two_digit_number[1])  # Pull out and convert character number 2 from string to integer class
result = char_1 + char_2
print(result)
```

_**Solution 3:**_

```python
two_digit_number = input("Type a two digit number: ")
char_1, char_2 = two_digit_number[0], two_digit_number[1]
result = int(char_1) + int(char_2)
print(result)
```

### 1.5. Lower() function

> #### _Arithmetic operators are used with numeric values to perform common mathematical operations:_

- **Addition** (+) 
- **Subtraction** (-) 
- **Multiplication** (*)
- **Division** (/)
- **Exponentiation** (**)

_**Examples:**_

```python
print(2 + 2)
```


```python
print(4 - 2)
```

```python
print(2 * 2)
```

```python
print(6 / 2)
```

```python
print(3 ** 2)
```

#### PEMDAS is the level of execution priority

The range from the highest to the lowest priority:

**P** is parentheses.  
**E** is exponentiation.  
**M** is multiplication.  
**D** is division.  
**A** is addition.  
**S** is subtraction. 

#### BUT

Multiplication = Division, and have the same level of priority  
Addition = Subtraction, and have the same level of priority

>#### _In this situation, execution goes from the left side of the example to the right._

### 1.6. Count() function

> #### _The round() function returns a floating point number that is a rounded version of the specified number, with the specified number of decimals._

The default number of decimals is 0, meaning that the function will return the nearest integer.

_**Example 1:**_

```python
x = round(5.2)
print(x)  # Returns 5
```

_**Example 2:**_

```python
x = round(5.7)
print(x)  # Returns 6
```

We can assign how many number of decimals to use when rounding the number.

_**Example 1:**_

```python
x = round(5.589, 2)
print(x)  # Returns 5.59
```

```python
x = round(75.98991458, 3)
print(x)  # Returns 75.99
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






 

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[TO THE DAY 1 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%201.md)
