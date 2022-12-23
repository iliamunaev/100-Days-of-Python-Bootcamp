# 100 projects in one file

>**Day 1:** "Band name generator", "Username generator".  
>**Day 2:** "Tip calculator", "Service price calculator".  
>**Day 3:** "Pizza order program", "Love calculator", "Treasure Island".  
>**Day 4:** "Hide the treasure", "Rock, Paper, Scissors".
>**Day 5:** "Password Generator".

## Day 1: "Band name generator", "Username generator"

### #1 Bootcamp day project: "Band name generator"

Write a greeting for your program. Ask the user for the city that they grew up in.  
Ask the user for the name of a pet.Combine the name of their city and pet and show them their band name.  
Make sure the input cursor shows on a new line:

_**Solution:**_

```python
print("Welcom to the Band Name Generator.")
city = input("What's name of the city your grew up in? ")
pet_name = input("What's your pet's name? ")
band_name = city + " " + pet_name
print("Your band name could be: " + band_name)
```

### #2 My day project: "Username generator"

The username generator creates a username based on a first and a last name of the user.  
The uniqueness of the name is given also by the number added to the end of the name, which is a combination of two integers.  
The numbers are equivalent to the length of the first and the last name of the user.  

_**Solution:**_

```python
print('Welcome to the "Username Generator".')
first_name = input("Type in your first name: ")
last_name = input("Type in your last name: ")

# Count number of characters of the first and the last names
# and convert them from integer to string.
length_first_name = str(len(first_name))
length_last_name = str(len(last_name))
print("Your Username is: " + first_name + "_" + last_name + "_" + length_first_name + length_last_name)
```

---

## Day 2: "Tip calculator", "Service price calculator"

### #3 Bootcamp day project: "Tip calculator"

Write a program which calculates total price and split the bill between all participants.  
If the bill was $150.00, split between 5 people, with 12% tip.  
Each person should pay (150.00 / 5) * 1.12 = 33.6  
Format the result to 2 decimal places = 33.60

_**Solution:**_

```python
print("Welcom to the tip calculator.")
bill = float(input("What was the total bill? $"))
tip_persentage = int(input("What persentage tip would you lake to give? 10, 12 or 15? "))
number_of_people = int(input("How many people to split the bill? "))
tip_sum = tip_persentage * bill / 100
pay_sum = bill + tip_sum / number_of_people
sum_for_each = round((pay_sum / number_of_people),2)
print(f"Each person should pay: ${sum_for_each}")
```

### #4 My day project: "Service price calculator"

The calculator calculates the cost of the service based on the input data.  
It is assumed that the apartment always has at least 1 window and a door. No zero values are used.

_**Solution:**_

```python
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
```

---

## Day 3: "Pizza order program", "Love calculator", "Treasure Island"

### #5 Bootcamp day project 1: "Pizza order program"

Build an automatic pizza order program. Based on a user's order, work out their final bill.
Small Pizza: $15  
Medium Pizza: $20  
Large Pizza: $25  
Pepperoni for Small Pizza: +$2  
Pepperoni for Medium or Large Pizza: +$3  
Extra cheese for any size pizza: + $1  

_**Solution 1:**_

```python
print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")
bill = 0
if size == "S":
    bill += 15
    if add_pepperoni == "Y":
        bill += 2
    else:
        bill
    if extra_cheese == "Y":
        bill += 1
    else:
        bill
elif size == "M":
    bill += 20
    if add_pepperoni == "Y":
        bill += 3
    else:
        bill
    if extra_cheese == "Y":
        bill += 1
    else:
        bill
else:
    bill += 25
    if add_pepperoni == "Y":
        bill += 3
    else:
        bill
    if extra_cheese == "Y":
        bill += 1
    else:
        bill
print(f"Your final bill is: ${bill}.")
```

_**Solution 2:**_

```python
# Build an automatic pizza order program.
# Based on a user's order, work out their final bill.
# Small Pizza: $15
# Medium Pizza: $20
# Large Pizza: $25
# Pepperoni for Small Pizza: +$2
# Pepperoni for Medium or Large Pizza: +$3
# Extra cheese for any size pizza: + $1
print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")
bill = 0
if size == "S":
    bill += 15
elif size == "M":
    bill += 20
else:
    bill += 25
if add_pepperoni == "Y":
    if size == "S":
        bill += 2
    else:
        bill += 3
if extra_cheese == "Y":
    bill += 1
print(f"Your final bill is: ${bill}.")
```

### #6 Bootcamp day project 2: "Love calculator"

Write a program that tests the compatibility between two people. To work out the love score between two people:  
Take both people's names and check for the number of times the letters in the word TRUE occurs.  
Then check for the number of times the letters in the word LOVE occurs.   
Then combine these numbers to make a 2 digit number.  
For Love Scores less than 10 or greater than 90, the message should be: "Your score is **x**, you go together like coke and mentos."  
For Love Scores between 40 and 50, the message should be: "Your score is **y**, you are alright together."  

_**Solution:**_

```python
print("Welcome to the Love Calculator!")
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")
# Concatenate both names in a string.
names_of_couple = name1 + name2
# Change all letters to a lower case.
names_of_couple = names_of_couple.lower()
# Count the number of times each letter in the words TRUE and LOVE occurs.
# Count the total number of all occurred letters.
t_counted = names_of_couple.count("t")
r_counted = names_of_couple.count("r")
u_counted = names_of_couple.count("u")
e1_counted = names_of_couple.count("e")
true_total = t_counted + r_counted + u_counted + e1_counted
l_counted = names_of_couple.count("l")
o_counted = names_of_couple.count("o")
v_counted = names_of_couple.count("v")
e2_counted = names_of_couple.count("e")
love_total = l_counted + o_counted + v_counted + e2_counted
# Convert total numbers into string
# and concatenate them.
total = str(true_total) + str(love_total)
# Convert total numbers back into integer class.
total = int(total)
# State the conditions.
if total < 10 or total > 90:
    print(f"Your score is {total}, you go together like coke and mentos.")
elif 40 < total < 50:
    print(f"Your score is {total}, you are alright together.")
else:
    print(f"Your score is {total}.")
```

### #7 Bootcamp day project 3: "Treasure Island"

Make a game.Use conditionals such as if, else, and elif statements to lay out the logic and the story's path in your program.  
Text Snippets:  
"You're at a crossroad. Where do you want to go? Type 'left' or 'right'."  
You've come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.'  
"You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?"  
"It's a room full of fire. Game Over."  
"You found the treasure! You Win!"  
"You enter a room of beasts. Game Over."  
"You chose a door that doesn't exist. Game Over."  
"You get attacked by an angry trout. Game Over."  
"You fell into a hole. Game Over."  

_**Solution:**_

```python
print("Welcome to Treasure Island.\nYour mission is to find the treasure.")
choice_1 = input("Choose your path. Turn to the left or to the right. Type 'left' or 'right'\n")
choice_1 = choice_1.lower()
if choice_1 == "left":
    choice_2 = input("You have to cross the river. Do you want swim or wait for a boat? Type 'swim' or 'wait'\n")
    choice_2 = choice_2.lower()
    if choice_2 == "wait":
        choice_3 = input("Choose the door: red, blue or yellow. Type 'red', 'blue' or 'yellow'\n")
        choice_3 = choice_3.lower()
        if choice_3 == "red":
            print("Burned by fire. Game over!")
        elif choice_3 == "blue":
            print("Eaten by a warm. Game over!")
        else:
            print("You are win! Take an icecream!")
    else:
        print("You was attacked by shark. Game over!")
else:
    print("Fall into a hole. Game over!")
```

---

## Day 4: "Hide the treasure", "Rock, Paper, Scissors"

### #8 Bootcamp day project 1: "Hide the treasure"

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

### #9 Bootcamp day project 1: "Rock, Paper, Scissors"

Make a rock, paper, scissors game.  
You'll find the ASCII art for the hand signals already saved to a corresponding variable: rock, paper, and scissors.  
Start the game by asking the player: "What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors."  
You can find the "official" rules of the game on the [World Rock Paper Scissors Association website](https://wrpsa.com/the-official-rules-of-rock-paper-scissors/).

_**Solution:**_

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

## Day 4: "Password Generator"

### #10 Bootcamp day project: "Password Generator"

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
