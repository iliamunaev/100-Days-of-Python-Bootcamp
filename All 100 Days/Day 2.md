# Day 2: integer and int() function, float and float() function, boolean, type(), arithmetic operators, round()

> ## Day topics:
>
>[1.1. **Integer** definition and **int()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#11-integer-and-int-function)    
>[1.2. **Float** definition and **float()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#12-float-and-float-function)  
>[1.3. **Boolean** definition](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#13-boolean)  
>[1.4. **Type()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#14-type-function)  
>[1.5. **Arithmetic** operators](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#15-arithmetic-operators)  
>[1.6. **Round()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#16-round-function)  
>[1.7. **Day projects:** Tip Calculator, Service price calculator](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All%20100%20Days/Day%202.md#17-day-projects)  

### 1.1. Integer and int() function

> #### _Integers are zero, positive or negative whole numbers without a fractional part and having unlimited precisionintegers are zero, positive or negative whole numbers without a fractional part and having unlimited precision_

All integer literals or variables are objects of the int class.  

_**Example 1:**_

```python
# Those are integers
integer_one = 2
integer_two = 8974
integer_three = -894
```

Leading zeros in non-zero integers are not allowed e.g. 000123 is invalid number, 0000 is 0.  

_**Example 2:**_

```python
x=012
SyntaxError:leading zeros in decimal integer literals are not permitted
```

Python does not allow comma as number delimiter. Use underscore _ as a delimiter instead.  

_**Example 3:**_

```python
number_1 = 123_456_789
number_2 = 123456789
number_1 = number_2
```

> #### _Int() function returns an integer from a given object or converts a number in a given base to a decimal._

_**Example 1:**_

```python
# Convert a string "55" into an integer
num = int("55")
print(type(num))
```

_**Example 2:**_

```python
# Convert an input value string class into an integer class
num = int(input("Type in a number: "))
print(type(num))
```

_**Example 3:**_

```python
num = input("Type in a number: ")
num_as_int = int(num)
print(type(num_as_int))
```

#### Extract a character by index

You can get a character at the desired position by specifying an index in [ ].  
Indexes begin with 0 (zero-based indexing).

>Zero-based array indexing is a way of numbering the items in an array such that the first item of it has an index of 0,
>whereas a one-based array indexed array has its first item indexed as 1. 

_**Example:**_

```python
username = "MaxToronto"
print(username[0])  # Pull out "M"
print(username[1])   # Pull out "a"
print(username[3])   # Pull out "T"
```

### 1.2. Float and float() function

> #### _The float type in Python represents the floating point number._

Float is used to represent real numbers and is written with a decimal point dividing the integer and fractional parts. 

_**Example:**_

```python
# Those are float numbers
float_num_1 = 2.5
float_num_2 = 0.777
float_num_3 = -3.87
```

> #### _Float() function converts a number stored in a string or integer into a floating point number, or a number with a decimal point._

_**Example 1:**_

```python
# Convert a string "8.5" into an integer
num = float("8.5")
print(type(num))
```

_**Example 2:**_

```python
# Convert an input value string class into a float class
num = float(input("Type in a number: "))
print(type(num))
```

_**Example 3:**_

```python
num = input("Type in a number: ")
num_as_float = float(num)
print(type(num_as_float))
```

### 1.3. Boolean  

> #### _Boolean means a result that can only have one of two possible values: true or false._

Boolean logic takes two statements or expressions and applies a logical operator to generate a Boolean value that can be either true or false. 

![Boolean_logic_exaple](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/Boolean_logic.png)

When you compare two values, the expression is evaluated and Python returns the Boolean answer.

_**Example 1:**_

```python
print(10 > 9)  #Returns True
print(7 == 9)  #Returns False
print(1 < 9)  #Returns True
```

### 1.4. Type() function

> #### _Type() function returns the type of the objects/data elements stored in any data type ._
  
TIn Python, we do not explicitly specify the data type of the variable for storing data elements.  
Hence, if we want to find out what type of data is stored in a variable we use Python’s built-in type() function.

_**Example 1:**_

```python
username = "Sara"
age = 18
distance_marathon = 42.092
print(type(username))  # Returns <class 'str'>
print(type(age))  # Returns <class 'int'>
print(type(distance_marathon))  # Returns <class 'float'>
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

### 1.5. Arithmetic operators

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

### 1.6. Round() function

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

#### Bootcamp day project: Tip calculator

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

<https://www.tutorialsteacher.com/python/python-number-type>  
<https://www.w3schools.com/python/python_numbers.asp> 
<https://www.geeksforgeeks.org/python-int-function/>  
<https://www.geeksforgeeks.org/python-float-type-and-its-methods/>
<https://www.techtarget.com/whatis/definition/Boolean#:~:text=In%20computing%2C%20the%20term%20Boolean,are%20used.>  
<https://www.w3schools.com/python/python_booleans.asp>  
<https://www.geeksforgeeks.org/python-type-function/>  
<https://note.nkmk.me/en/python-str-extract/>  
<https://medium.com/analytics-vidhya/array-indexing-0-based-or-1-based-dd89d631d11c>  
<https://www.w3schools.com/python/gloss_python_arithmetic_operators.asp>  

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[TO THE DAY 1 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%201.md)
