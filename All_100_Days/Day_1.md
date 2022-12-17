# Day 1: string, variables, print(), input(), len(), \n, +

> ## Day topics:
>
>[1.1. **String** definition](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#11-string)    
>[1.2. **Print()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#12-print-function)  
>[1.3. Escape operator **\n**](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#13-escape-operator-n)  
>[1.4. Concatenate strings using **addition (+) operator**](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#14-concatenate-strings-using-operator-)  
>[1.5. **Input()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#15-input-function)  
>[1.6. **Len()** function](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#16-len-function)  
>[1.7. **Variables:** definition, naming, changing](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/All_100_Days/Day_1.md#17-variables-definition-naming-changing)  
>1.8. Day project

### 1.1. String

> #### **_The technical description of a string is: an array of characters. The informal view of a string is a sentence._**

Strings are almost always written in code as a quoted sequence of characters, i.e., "this is a string".  
Strings are useful for storing human-readable data, like sentences, or lists of alphabetical data, like the nucleic acid sequences of DNA.

![String exaple](/assets/images/String_Variable_Diagram_Middle_Aspect_Ratio.png)

### 1.2. Print() function

> #### **_The print() function prints the specified message to the screen, or other standard output device._**

The message can be a string, or any other object, the object will be converted into a string before written to the screen.

```python
print("Hello World")
print("This is my first code")
print("I live in Helsinki")
```

### 1.3. Escape operator \n  

> #### **_\n is a type of escape character that will create a new line when used._**

```python
print("Hello World.\nThis is my first code.\nI live in Helsinki.")
```

### 1.4. Concatenate strings using operator +

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

### 1.5. Input() function

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

### 1.6. Len() function

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
### 1.7. Variables: definition, naming, changing  

> #### **_Variable is a name that is used to refer to memory location._**

Python variable is the basic unit of storage in a program.  
A variable is created automatically when you assign a value to it.   
The equal sign (=) is used to assign values to variables.

_**Example 1:**_

```python
user = 'Piter'
```

_**Example 2:**_

```python
user = 'Piter'
print(user)
```
_**Example 3:**_

```python
user = input('Enter your name: ')
print(user)
```

#### Rules for Python variables:

- A variable name must start with a letter or the underscore character.
- A variable name cannot start with a number.
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ ).
- Variable names are case-sensitive (age, Age and AGE are three different variables).

### Resources:

<https://en.wikipedia.org/wiki/String_(computer_science)>  
<https://www.w3schools.com/python/ref_func_print.asp>  
<https://realpython.com/python-print/>  
<https://careerkarma.com/blog/python-concatenate-strings/>  
<https://www.geeksforgeeks.org/taking-input-in-python/>  
<https://docs.python.org/3/library/functions.html#input>  
<https://www.w3schools.com/python/gloss_python_variable_names.asp>  






