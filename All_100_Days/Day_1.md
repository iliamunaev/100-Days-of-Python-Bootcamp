# Day 1

> ## Day goals:
>
>1.1. **String** definition   
>1.2. **print()** function  
>1.3. **\n** escape operator  
>1.4. Concatenate strings using **+** operator



### 1.1. String

> #### **_The technical description of a string is: an array of characters. The informal view of a string is a sentence._**

Strings are almost always written in code as a quoted sequence of characters, i.e., "this is a string".  
Strings are useful for storing human-readable data, like sentences, or lists of alphabetical data, like the nucleic acid sequences of DNA.

![String exaple](/assets/images/String_Variable_Diagram_Middle_Aspect_Ratio.png)

### 1.2. Print() function

> #### **_The print() function prints the specified message to the screen, or other standard output device._**

The message can be a string, or any other object, the object will be converted into a string before written to the screen.

Input:

```python
print("Hello World")
print("This is my first code")
print("I live in Helsinki")
```

Output:

![print_function_ex_1](/assets/giphy/print_function_ex_1.gif)

### 1.3. \n escape operator  

> #### **_\n is a type of escape character that will create a new line when used._**

Input:

```python
print("Hello World.\nThis is my first code.\nI live in Helsinki.")
```

Output:

![print_function_ex_1](/assets/giphy/print_function_ex_2.gif)

### 1.4. Concatenate strings using operator +

> #### **_The + operator (or addition operator) lets you combine two or more strings._**
  
This operator is referred to as the Python string concatenation operator.  
The + operator should appear between the two strings you want to merge.  
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

### Resources:

<https://en.wikipedia.org/wiki/String_(computer_science)>  
<https://www.w3schools.com/python/ref_func_print.asp>  
<https://realpython.com/python-print/>  
<https://careerkarma.com/blog/python-concatenate-strings/>  





