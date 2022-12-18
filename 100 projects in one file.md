# 100 projects

## Day 1: Username generator

```python
# The username generator creates a username based on a first and a last name of the user.
# The uniqueness of the name is given also by the number added to the end of the name
# which is a combination of two integers.
# The numbers are equivalent to the length of the first and the last name of the user.
print('Welcome to the "Username Generator".')
first_name = input("Type in your first name: ")
last_name = input("Type in your last name: ")

# Count number of characters of the first and the last names
# and convert them from integer to string.
length_first_name = str(len(first_name))
length_last_name = str(len(last_name))
print("Your Username is: " + first_name + "_" + last_name + "_" + length_first_name + length_last_name)
````
