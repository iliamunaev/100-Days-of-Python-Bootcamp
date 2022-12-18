# 100 projects in one file

>[**Day 1:** Band name generator, Username generator](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/100%20projects%20in%20one%20file.md#day-1-band-name-generator-username-generator)  
>[**Day 2:** Tip calculator, Service price calculator](https://github.com/iliamunaev/100-Days-of-Python-Bootcamp/edit/main/100%20projects%20in%20one%20file.md#day-2-tip-calculator-service-price-calculator)  

## Day 1: Band name generator, Username generator

### Bootcamp day project: Band name generator

```python
# 1. Create a greeting for your program.
# 2. Ask the user for the city that they grew up in.
# 3. Ask the user for the name of a pet.
# 4. Combine the name of their city and pet and show them their band name.
# 5. Make sure the input cursor shows on a new line:

print("Welcom to the Band Name Generator.")
city = input("What's name of the city your grew up in? ")
pet_name = input("What's your pet's name? ")
band_name = city + " " + pet_name
print("Your band name could be: " + band_name)
````

### My day project: Username generator

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

---

## Day 2: Tip calculator, Service price calculator

### Bootcamp day project: Tip calculator

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

### My day project: Service price calculator

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
