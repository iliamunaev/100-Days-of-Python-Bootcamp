#  **Day 8 (Part 1): "**Caesar cipher**" programming (step-by-step guide)**



## The task of the day is to create the Caesar cipher.



In cryptography, a Caesar cipher, the shift cipher, is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plain text is replaced by a letter some fixed number of positions down the alphabet. For example, with a left shift of 3, D would be replaced by A, E would become B, and so on. The method is named after Julius Caesar, who used it in his private correspondence.

More about Caesar cipher algorithm in [the link.](https://en.wikipedia.org/wiki/Caesar_cipher)

<img src="https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/images/Caesar_cipher_shift.png" width=70% height=70%>
*_Picture from <https://en.wikipedia.org/wiki/Caesar_cipher>_*

> ### Step 1: Plan the game structure.

Create a flowchart that represents the process of passing the game.

<img src="https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/assets/diagrams/caesar_cipher_flowchart.png">

> ### Step 2: Create an encrypt() function.

_**Pre-created data:**_

```python 
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 
            'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v',
            'w', 'x', 'y', 'z'
           ]

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))
```

Create a function called 'encrypt' that takes the 'text' and 'shift' as inputs.  
Inside the 'encrypt' function, shift each letter of the 'text' forwards in the alphabet by the shift amount and print the encrypted text. 

```python 
# Raw code. It will be rewritten later.
def encrypt(user_text, user_shift):
    cipher_text = ""
    
# Check all characters in the input text.
# Extract the index of each character.
    for letter in text:
        letter_index = alphabet.index(letter)
        
# Arrange a new index for each character.
        letter_index += shift

# Until a new index out of alphabet list's range use while loop.
        while letter_index > len(alphabet) - 1:
        
# In fact, using % modulo will be easier.
# But I realised it later.
            letter_index = letter_index - len(alphabet)
        new_letter = alphabet[letter_index]
        
# Arrange a new variable that contains ciphered characters.
        cipher_text += new_letter
    
    print(f"The encoded text is: '{cipher_text}'.")
```

Call the encrypt function and pass in the user inputs. You should be able to test the code and encrypt a message.

```python
encrypt(user_text=text, user_shift=shift)
```

> ### Step 3: Create a decrypt() function.

Create a different function called 'decrypt' that takes the 'text' and 'shift' as inputs.  
Inside the 'decrypt' function, shift each letter of the 'text' *backwards* in the alphabet by the shift amount and print the decrypted text.

```python
# The function decrypt() is created on the base of the encrypt() function.
# Raw code. It will be rewritten later.
def decrypt(user_text, user_shift):
    decoded_text = ""
    for letter in text:
        letter_index = alphabet.index(letter)
        letter_index -= shift
        while letter_index < 0:
            letter_index = letter_index + len(alphabet)
        new_letter = alphabet[letter_index]
        decoded_text += new_letter
    print(f"The decoded text is {decoded_text}")
    

decrypt(cipher_text=text, decoded_shift=shift)
```

> ### Step 4:  Call the functions.

Check if the user wants to encrypt or decrypt the message by checking the 'direction' variable.  
Then call the correct function based on that 'direction' variable. You should be able to test the code to encrypt and decrypt a message.

```python 
directionif direction == "encode":
    encrypt(user_text=text, user_shift=shift)
else:
    decrypt(cipher_text=text, decoded_shift=shift)
```

> ### Step 5: Combine encrypt() and decrypt() functions in one code.

```python
def encrypt(user_text, user_shift):
    cipher_text = ""
    for letter in text:
        letter_index = alphabet.index(letter)
        letter_index += shift
        while letter_index > len(alphabet) - 1:
            letter_index = letter_index - len(alphabet) - 1
        new_letter = alphabet[letter_index]
        cipher_text += new_letter
    print(f"The encoded text is: '{cipher_text}'.")

def decrypt(cipher_text, decoded_shift):
    decoded_text = ""
    for letter in text:
        letter_index = alphabet.index(letter)
        letter_index -= shift
        while letter_index < 0:
            letter_index = letter_index + len(alphabet)
        new_letter = alphabet[letter_index]
        decoded_text += new_letter
    print(f"The decoded text is {decoded_text}")


if direction == "encode":
    encrypt(user_text=text, user_shift=shift)
else:
    decrypt(cipher_text=text, decoded_shift=shift)

```

> ### Step 6: Replace a part of the code with % modulo.

```python
def encrypt(user_text, user_shift):
    cipher_text = ""
    for letter in text:
        character_index = alphabet.index(character)
        new_character = character_index + expected_shift
        while new_character > 25:
            
# Use % modulo.
            new_character = new_character % 26
            text_output += alphabet[new_character]
     print(f"The encoded text is: '{cipher_text}'.")
```

```python
def decrypt(cipher_text, decoded_shift):
    decoded_text = ""
    for letter in text:
        character_index = alphabet.index(character)
        new_character = character_index - expected_shift
        while new_character < 0:
            
# Use % modulo.
            new_character = new_character % 26
            text_output += alphabet[new_character]
            print(f"The decoded text is {decoded_text}")
     print(f"The decoded text is {decoded_text}")
```

> ### Step 7: Combine encrypt() and decrypt() into a single caesar() function.

Call the caesar() function, passing over the 'text', 'shift' and 'direction' values.

```python
# Arrange new names for variables. 
def caesar(typed_message, expected_shift, method):
    text_output = ""

# for loop uses for both methods. 
    for character in typed_message:
        
        if method == "encode":
            character_index = alphabet.index(character)
            new_character = character_index + expected_shift
            while new_character > 25:
                new_character = new_character % 26
                text_output += alphabet[new_character]

            else:
                character_index = alphabet.index(character)
                new_character = character_index - expected_shift
                while new_character < 0:
                    new_character = new_character % 26
                    text_output += alphabet[new_character]

# Common print output for both results.
    print(f"The {method}d text is: '{text_output}'.")
    
caesar(typed_message=text, expected_shift=shift, method=direction)
```

> ### Step 8: Allow the user to use other symbols.

Those symbols will not be ciphered.

```python
for character in typed_message:
        if character in alphabet:            
            if method == "encode":
                #code
            else:
                #code
        else:
            text_output += character
```

> ### Step 9: Deploy the new part of the code into the caesar() function.

```python
def caesar(typed_message, expected_shift, method):
    text_output = ""

    for character in typed_message:

# Check the presence of the character in the input text.
        if character in alphabet:
            if method == "encode":
                character_index = alphabet.index(character)
                new_character = character_index + expected_shift
                while new_character > 25:
                    new_character = new_character % 26
                text_output += alphabet[new_character]

            else:
                character_index = alphabet.index(character)
                new_character = character_index - expected_shift
                while new_character < 0:
                    new_character = new_character % 26
                text_output += alphabet[new_character]

# Other characters than those in the alphabet list are not ciphered.  
        else:
            text_output += character

    print(f"The {method}d text is: '{text_output}'.")
    
    
caesar(typed_message=text, expected_shift=shift, method=direction)
```

> ### Step 10: Restart possibility.

Allow the user to restart "Caesar cipher".

```python
# Assign the condition
should_end = False
while not should_end:

    direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n").lower()
    text = input("Type your message:\n").lower()
    shift = int(input("Type the shift number:\n"))

    caesar(typed_message=text, expected_shift=shift, method=direction)

# Ask the user if they want to restart.  
    restart = input("Type 'yes' if you want to restart again. Otherwise type 'no'.\n").lower()
    if restart == "no":
        should_end = True
        print("See you!")
```

> ### Step 12: Final code.

Combine all codes into the final code. 

```python
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 
            'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v',
            'w', 'x', 'y', 'z'
           ]


def caesar(typed_message, expected_shift, method):
    text_output = ""

    for character in typed_message:
        if character in alphabet:
            if method == "encode":
                character_index = alphabet.index(character)
                new_character = character_index + expected_shift
                while new_character > 25:
                    new_character = new_character % 26
                text_output += alphabet[new_character]

            else:
                character_index = alphabet.index(character)
                new_character = character_index - expected_shift
                while new_character < 0:
                    new_character = new_character % 26
                text_output += alphabet[new_character]

        else:
            text_output += character

    print(f"The {method}d text is: '{text_output}'.")


should_end = False
while not should_end:

    direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n").lower()
    text = input("Type your message:\n").lower()
    shift = int(input("Type the shift number:\n"))

    caesar(typed_message=text, expected_shift=shift, method=direction)

    restart = input("Type 'yes' if you want to restart again. Otherwise type 'no'.\n").lower()
    if restart == "no":
        should_end = True
        print("See you!")
```

---

### Resources:

<https://en.wikipedia.org/wiki/Caesar_cipher>  

---

[> to Glossary](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/Glossary.md)  
[> to all 100 projects](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/100%20projects%20in%20one%20file.md)

[DAY 7 <](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/blob/main/All%20100%20Days/Day%207.md)
