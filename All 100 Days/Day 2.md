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

> #### **_Integers are zero, positive or negative whole numbers without a fractional part and having unlimited precisionintegers are zero, positive or negative whole numbers without a fractional part and having unlimited precision_**

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

> #### **_Int() function returns an integer from a given object or converts a number in a given base to a decimal._**

_**Example 1:**_

```python
# Convert a string "5.5" into an integer
num = int("5.5")
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

### 1.2. Float and float() function

> #### **_The float type in Python represents the floating point number._**

Float is used to represent real numbers and is written with a decimal point dividing the integer and fractional parts. 

_**Example:**_

```python
# Those are float numbers
float_num_1 = 2.5
float_num_2 = 0.777
float_num_3 = -3.87
```

> #### **_Float() function converts a number stored in a string or integer into a floating point number, or a number with a decimal point. _**

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

> #### **_\n is a type of escape character that will create a new line when used._**

```python
print("Hello World.\nThis is my first code.\nI live in Helsinki.")
```

### 1.4. Type() function

> #### **_The (+) operator (or addition operator) lets you combine two or more strings._**
  
The addition operator (+) is referred to as the Python string concatenation operator.  
The operator should appear between the two strings you want to merge.  
Don't forget to add space between words in the sentence.

_**Solution 1:** adding space at the end of the first word inside the brackets_

```python
print("Hello " + "World")
```

_**Solution 2:** adding space at the beginning of the second word inside the brackets_

```python
print("Hello" + " World")
```

_**Solution 3:** adding space between the words using space inside a new pair of brackets_

```python
print("Hello" + " " + "World")
```

### 1.5. Arithmetic operators

> #### **_The input() function reads a line from input, converts it to a string, and returns that._**

The function is a way of asking the user to provide some type of input.
When the input function is called it stops the program and waits for the user’s input. 
When the user presses enter, the program resumes and returns what the user typed. 

_**Example 1:**_

```python
input('Enter your name: ')
```
_**Example 2:**_

```python
print(input('Enter your name: '))
```

### 1.6. Round() function

> #### **_The len() function return the length (the number of items) of an object._**

The function is a way of asking the user to provide some type of input.
When the input function is called it stops the program and waits for the user’s input. 
When the user presses enter, the program resumes and returns what the user typed. 

_**Example 1:**_

```python
len('Markus')
```
_**Example 2:**_

```python
print(len('Markus'))

```

### 1.7. Day projects

#### Bootcamp day project: Tip calculator

```python
# If the bill was $150.00, split between 5 people, with 12% tip. 
# Each person should pay (150.00 / 5) * 1.12 = 33.6
# Format the result to 2 decimal places = 33.60
# Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.💪

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
pets = int(input("Do you have pats in the apartment? If no type in '0', if you have type in '1': "))
price_base = 15

# Calculating a cost based on the input and multiplying on indexes if applicable
price_on_square = price_base * square
price_on_windows = price_base * windows * 1.4
price_on_doors = price_base * doors * 1.2
price_on_pets = price_base * pets * 20
price = price_on_square + price_on_windows + price_on_doors + price_on_pets

# Calculating a cost based on the start date of the service
price_urgent = price * 1.3
print(f"Total price for cleaning service is:\nWe start tomorrow or later: {price}\nWe start today: {price_urgent}")
print("Call us now and get 10% discount!")
````

---

### Resources:

<https://www.tutorialsteacher.com/python/python-number-type>  
<https://www.w3schools.com/python/python_numbers.asp> 
<https://www.geeksforgeeks.org/python-int-function/>  
<https://www.geeksforgeeks.org/python-float-type-and-its-methods/>



---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[TO THE DAY 1 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%201.md)





