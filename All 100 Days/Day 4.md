# Day 4: Conditional statements: if, elif, else; Comparison operators: >, <, >=, <=, ==, !=; Modulo %; Logical operators: and, or, not; Lower(); Count(); Day projects: Pizza order program, Love calculator; Treasure Island.



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

