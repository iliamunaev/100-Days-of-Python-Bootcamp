# Day 2: integer and int() function, float and float() function, boolean, type(), arithmetic operators, round()

> ## Day topics:
>
>[1.1. **Integer** definition](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#11-string)    
>[1.2. **Float** definition](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#12-print-function)  
>[1.3. **Boolean** definition](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#13-escape-operator-n)  
>[1.4. **Type()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#14-concatenate-strings-using-operator-)  
>[1.5. **Arithmetic** operators](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#15-input-function)  
>[1.6. **Round()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#16-len-function)  
>[1.7. **Day projects:** Tip Calculator, Service price calculator](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#18-day-project-username-generator)  

### 1.1. Integer and int() function

> #### **_The technical description of a string is: an array of characters. The informal view of a string is a sentence._**

Strings are almost always written in code as a quoted sequence of characters, i.e., "this is a string".  
Strings are useful for storing human-readable data, like sentences, or lists of alphabetical data, like the nucleic acid sequences of DNA.

![String exaple](/assets/images/String_Variable_Diagram_Middle_Aspect_Ratio.png)

### 1.2. Float and float() function

> #### **_The print() function prints the specified message to the screen, or other standard output device._**

The message can be a string, or any other object, the object will be converted into a string before written to the screen.

```python
print("Hello World")
print("This is my first code")
print("I live in Helsinki")
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
##If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
#Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.💪

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

<https://en.wikipedia.org/wiki/String_(computer_science)>  
<https://www.w3schools.com/python/ref_func_print.asp>  
<https://realpython.com/python-print/>  
<https://careerkarma.com/blog/python-concatenate-strings/>  
<https://www.geeksforgeeks.org/taking-input-in-python/>  
<https://docs.python.org/3/library/functions.html#input>  
<https://www.w3schools.com/python/gloss_python_variable_names.asp>  

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[>TO THE DAY 2]





