# Day 7: "Hangman" game programming (step-by-step guide)

## The task of the day is to create the Hangman game. 

Hangman game ruls in [the link.](https://www.wikihow.com/Play-Hangman)

_**Briefly:**_

Hangman is a quick and easy game for at least two people.  
One player, the "host," makes up a secret word, while the other player tries to guess the word by asking what letters it contains.  
However, every wrong guess brings them one step closer to losing. 

<img src = "https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/hangman.jpg">

_Picture from <https://www.wikihow.com/Play-Hangman>_

> ### Step 1: Plan the game structure.

 Create a flowchart that represents the process of passing the game.

<img src = "https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/diagrams/hangman_flowchart.png">

---

> ### Step 2: Random word selection.

Create a list of words and save it as Python (.py) file.  
Create a code for the randomly chosen word. 

```python
# Create a list 'word_list', and save it in a hangman_words.py.  
# Fill word_list with words which will be used in the game.
# For the real game, choose more words -)
word_list = [
    'axiom',
    'cycle',
    'jazz',
    'youthful'
]
```

```python
# Import the' random' module, which implements pseudo-random number generators for various distributions.
import random

# Import all words from the saved file. 
from hangman_words import word_list

# Use the .choice() method to return a randomly selected element from the word_list. 
random_word = random.choice(word_list)
```

---

> ### Step 3: Receive a letter from the user.

Ask the user to guess a letter.  
Make the letter lowercase.  

```python
# Use the .lower() method to return a string where all characters are lowercase.
letter = input("Please type in a letter: ").lower()
```

---

> ### Step 4: Blank list visualisation.

A blank list is a list with a number of empty spaces equivalent to the number of letters in the chosen word.
It should be shown to the user.

```python
# Assign an empty list.
blanked_list = []

# Use therange() function to return a sequence of numbers, starting from 0 by default.
# Use for loop for iterating over a sequence in the 'random_word' string.
for n in range(len(random_word)):
    blanked_list += "_"
```

---

> ### Step 5: Replace letters in the blank list.

If the letter was chosen and is present in the word, the empty space in the blank list should be replaced by the letter in the right place.

```python
for n in range(len(random_word)):
    if letter == random_word[n]:
        blanked_list[n] = letter
        print(blanked_list)
```

---

> ### Step 6: Loop for returning the user to guess the next letter (proper letter).

Every time when the user chooses the proper letter, the user should be asked to guess the next letter.

```python

game_over = False

while not game_over:
    letter = input("Please type in a letter: ").lower()
    for n in range(len(random_word)):
        if letter == random_word[n]:
            blanked_list[n] = letter
            print(blanked_list)
```

---

> ### Step 7: Assign the game over criterion (possibility 1).

Assign a criterion for the end of the game based on guessing all the letters.

```python

game_over = False

while not game_over:
    letter = input("Please type in a letter: ").lower()
    for n in range(len(random_word)):
        if letter == random_word[n]:
            blanked_list[n] = letter
            print(blanked_list)

# The game over criterion            
    if "_" not in blanked_list:
        game_over = True
        print("You win!")
```

---

> ### Step 8: Create pics of all game stages.

Visualize stages which will be shown to the user if the user chooses the wrong letter.  
Save a visualization in a list of words as a Python (.py) file.

```python
# Create a list 'stages', and save it in a hangman_art.py.
stages = [
    '''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
'''
]
```

---

> ### Step 9: Loop for returning the user to guess the next letter (wrong letter).

Every time when the user chooses the wrong letter, the user should be asked to guess the next letter.  
A picture of the current stage should be shown.

```python
# Import visualisation 'stages' from the saved file. 
from hangman_art import stages

game_over = False

# Assing index of elements in 'stage' list as a 'stage_index'.
# stage_index starts to count in the loop from '5' to '0' according to the corresponding stages.
stage_index = 5

while not game_over:
    letter = input("Please type in a letter: ").lower()

# Assign the criterion for returning the user to guess the next letter.
    if letter not in random_word:
        print(stages[stage_index])
        print(f"'{letter}' is not in the word.")
        stage_index -= 1
        
    for n in range(len(random_word)):
        if letter == random_word[n]:
            blanked_list[n] = letter
            print(blanked_list)
            
    if "_" not in blanked_list:
        game_over = True
        print("You win!")        
```

---

> ### Step 10: Assign the game over criterion (possibility 2).

Assign the game over criterion based on losing the game.

```python
game_over = False

while not game_over:
    letter = input("Please type in a letter: ").lower()
    if letter not in random_word:
        print(stages[stage_index])
        print(f"'{letter}' is not in the word.")
        stage_index -= 1
        
    for n in range(len(random_word)):
        if letter == random_word[n]:
            blanked_list[n] = letter
            print(blanked_list)
            
    if "_" not in blanked_list:
        game_over = True
        print("You win!")
 
 # Assign the game over criterion.
    if stage_index < 0:
        game_over = True
        print("You lose!")
```

---

> ### Step 11: Give a chance to the user if the user has already chosen the letter before.

If the user has entered a letter they've already guessed, print it and let them know.  
Do not count the attempt as a wrong answer.

```python
if letter in blanked_list:
    print(f"You have already chosen the letter '{letter}'. Try again!")
```

---

> ### Step 12: Final code.

```python
# Import all you need.
from hangman_words import word_list
from hangman_art import stages
import random

# Assign all variables.
blanked_list = []
game_over = False
stage_index = 5

# Start the game by choosing a random word.
random_word = random.choice(word_list)

# Create a blank list with empty spaces instead of letters. 
for n in range(len(random_word)):
    blanked_list += "_"

# Create the main loop and ask the user to guess a letter.
while not game_over:
    print(blanked_list)
    letter = input("Please type in a letter: ").lower()

# Inform the user if they already chose the letter before.
    if letter in blanked_list:
        print(f"You have already chosen the letter '{letter}'. Try again!")

# Conditions when the user chooses the wrong letter.
    if letter not in random_word:
        print(stages[stage_index])
        print(f"'{letter}' is not in the word.")        
        stage_index -= 1

# Conditions when the user chooses the proper letter.
# Replace blanked places with letters.
    for n in range(len(random_word)):
        if letter == random_word[n]:
            blanked_list[n] = letter            

# Game over conditions.
    if "_" not in blanked_list:
        game_over = True
        print("You win!")
    if stage_index < 0:
        game_over = True
        print("You lose!")
```

_PS: the most last step, which allows the user decides whether to continue playing the game or quit, was not covered by the final code._

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[DAY 6 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%206.md)
