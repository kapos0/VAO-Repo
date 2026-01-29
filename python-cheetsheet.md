# Python Cheat Sheet

## General

### Comments

```python
# This is a comment
print("Hello, World!")

"""
This is a comment
written in
more than just one line
"""

```

## Print & Input

### Print

```python
print("Hello world!")

message = "SheCodes"
print(message)

```

### Input

```python
first_name = input("What is your first name")
last_name = input("What is your last name")
full_name = firstName + " " + lastName
print(full_name)

```

## Variables

### Variable creation

```python
school = "SheCodes"
full_package = "SheCodes Pro"
projects = 4
awesome = true

```

### Variable operations

```python
x = 2
y = 3
z = x + y # 5

city = "Lisbon"
country = "Portugal"
place = city + " " + country # Lisbon Portugal

```

## Strings

### String creation

```python
greetings = "Good morning!"
sentence = "it's sunny today"

```

### String length

```python
sentence = "it's sunny today"
print(len(sentence)) # 16

```

### Access string characters

```python
sentence = "it's sunny today"

print(sentence[0]) # i
print(sentence[0:10]) # it's sunny

```

### Concatenation

```python
greetings = "Good morning!"
sentence = "it's sunny today"

print(greetings + " " + sentence.capitalize())

```

### String methods

```python
print("hello".capitalize()) # Hello
print("hello".upper()) # HELLO
print("Hello".lower()) # hello
print(" Hello      ".strip().upper()) # HELLO
print("Hello".strip("o")) # Hell
print("Hello".count("l")) # 2
print("Hello".replace('l', 'x')) # Hexxo

```

### f Strings

```python
greetings = "Good morning!"
sentence = "it's sunny today"

print(f"{greetings} {sentence.capitalize()}.") # Good morning! It's sunny today.

```

## Numbers

### Integers

```python
months = 12
print(months)

```

### Float

```python
pi = 3.14159265358979323
print(pi)

```

### Arithmetic

```python
print(2 + 2)
print(2 - 2)
print(2 * 2)
print(2 / 2)
print(2 ** 2)

a = 10
b = 3
print(a * b / 2)

```

### Pow

```python
result = pow(2, 3) 
print(result) # 8

```

### Abs

```python
absolute = abs(-10) 
print(absolute) # 10

```

### Round

```python
price = 99
discount = 18.15
discounted_price = price - price * discount / 100
print(round(discounted_price))

```

## Data type conversion

### Convert a string into an integer

```python
temperature = "12"
temperature = int(temperature)

print(temperature + 10)

temperature = input("What is the temperature? ")
temperature = int(temperature)
print(f"Tonight it will be {temperature - 10} degrees")

```

### Convert a string into a float

```python
temperature = "12.5"
temperature = float(temperature)

print(temperature + 10)

```

### Convert integer or float into a string

```python
temperature  = 12
temperature = str(temperature)
print("It is currently "  + temperature + " degrees")

```

## If else

### Comparison Operators

```python
a = 1
b = 2  
print(a == b) # equal to => False
print(a != b) # not equal to => True
print(a > b) # greater than => False
print(a < b) # less than => True
print(a >= b) # greater than or equal to => False
print(a <= b) # less than or equal to => True

```

### Logical Operators

```python
# Logical Operators
# and, or, not
print(a == 1 and b == 2) # True
print(a == 2 and b == 2) # False
print(a == 1 or b == 3) # True
print(a == 4 or b == 0) # False
print(not(a == 2)) # True

```

### Booleans

```python
open = True
closed = False

```

### If else statements

```python
age = input("How are old are you? ")
age = int(age)

if age >= 65 and age <= 90:
  print("You are wize")

if age < 18:
  print("You cannot vote")
  print(f"because you are {age} years old")
else:
  print("You're old enough to vote, congrats! 👏")

if age >= 21:
  print("You can party")
else:
  print("Stay home, you're too young to party")

```

### If-Elif-Else statements

```python
temperature = input("What's the temperature outside? ")
temperature = int(temperature)

if temperature > 30: 
  print("It's warm")
elif temperature >= 20:
  print("It's nice")
elif temperature >= 10:
  print("It's chilly")
else:
  print("It's cold")

```

## Lists

### List Creation

```python
# List of strings
students = ["Luiza", "Maria", "Sara", "Daniela"]
# List of numbers
numbers = [1, 3, 5, 10]
# Empty list
certificates = []

```

### Access a list element

```python
# Access an element of the list
# Index starts at 0, not 1
print(students[0]) # => Luiza
print(students[1]) # => Maria

```

### List Length

```python
print(len(students)) # => 4

```

### Update element from a List

```python
students[1] = "Julie"
print(students) # => ["Luiza", "Julie", "Sara", "Daniela"]

```

### Add Element to a List

```python
# Add an element to the list
students.append("Sofia")
print(students) # => ["Luiza", "Julie", "Sara", "Daniela", "Sofia"]
students.insert(0, "Matilde")
print(students) # => ["Matilde", "Luiza", "Julie", "Sara", "Daniela", "Sofia"]

```

### Remove List Element

```python
students.remove("Daniela")
print(students) # => ["Matilde", "Luiza", "Julie", "Sara", "Sofia"]
students.pop()
print(students) # => ["Matilde", "Luiza", "Julie", "Sara"]
students.pop(2)
print(students) # => ["Matilde", "Luiza", "Sara"]
del students[1]
print(students) # => ["Matilde", "Sara"]

```

### Order a List

```python
students = ["Luiza", "Maria", "Sara", "Daniela"]
students.sort()
print(students) # => ["Daniela", "Luiza", "Maria", "Sara"]
students.reverse()
print(students) # => ["Sara", "Maria", "Luiza", "Daniela"]

```

### List for loops

```python
students = ["Maria", "Sara", "Daniela", "Julie", "Luiza"]

for student in students:
  print(f"The student name is {student.title()}.")

```

## Dictionaries

### Dictionary declaration

```python
# Creating an empty dictionary
winners = {}

# Creating a dictionary with key-value pairs
temperatures = {"Lisbon": 12, "Paris": 15, "Madrid": 35}

```

### Access a dictionary element

```python
temperatures = {"Lisbon": 12, "Paris": 15, "Madrid": 35}

# Accessing a value
print(temperatures["Madrid"]) # => 35
print(temperatures["Lisbon"]) # => 12
print(temperatures.get("Lisbon")) # => 12
print(temperatures.get("New York")) # => None

```

### Adding a key-value pair to dictionary

```python
# Creating a dictionary with key-value pairs
temperatures = {"Lisbon": 12, "Paris": 15, "Madrid": 35}

# Adding a key-value pair
temperatures["New York"] = 2
print(temperatures) # {'Lisbon': 12, 'Paris': 15, 'Madrid': 35, 'New York': 2}

```

### Modifying a dictionary value

```python
# Creating a dictionary with key-value pairs
temperatures = {"Lisbon": 12, "Paris": 15, "Madrid": 35}

# Modify a value
temperatures["Lisbon"] = 25
print(temperatures["Lisbon"]) # => 25

```

### Removing key value pair from dictionary

```python
temperatures = {"Lisbon": 12, "Paris": 15, "Madrid": 35}

# Removing key-value pair
del temperatures["Lisbon"]
print(temperatures) # {'Paris': 15, 'Madrid': 35, 'New York': 2}
temperatures.pop("Paris")
print(temperatures) # {'Madrid': 35, 'New York': 2}
temperatures.popitem()
print(temperatures) # {'Madrid': 35}

```

### Dictionary for loops

```python
temperatures = {"Lisbon": 22, "London": 10, "Sydney": 32}

# Looping through each key
for city in temperatures:
  temperature = temperatures[city]
  print(f"The temperature in {city} is {temperature} degrees")

# Better: Looping through each key-value pair
for city, temperature in temperatures.items():
  print(f"The temperature in {city} is {temperature} degrees")

```

## Dates

### Current date and time

```python
from datetime import datetime

now = datetime.now()
print(now)

```

### Create a date manually

```python
from datetime import datetime

date = datetime(2034, 1, 24, 4, 0, 12)
print(date)

```

### Convert a date to a string

```python
from datetime import datetime

formatted_date = date.strftime("See you on %d %B %Y at %-I%p")
print(formatted_date)

```

### Get a timestamp from a date

```python
from datetime import datetime

print(now.timestamp())

```

### Create a date from a timestamp

```python
from datetime import datetime

timestamp = 1705590204
date_from_timestamp = datetime.fromtimestamp(timestamp)
print(date_from_timestamp)

```

## Functions

### Function declaration

```python
def say_hello_world():
  name = input("What is your name? ")
  if name:
    print(f"Hello {name.capitalize()}!")
  else:
    print("Too bad you don't have a name")


say_hello_world()
say_hello_world()

```

### Function Arguments

```python
def greet_user(first_name, last_name):
  """Welcome the user"""
  full_name = first_name + " " + last_name
  print(f"Hello {full_name}!")

greet_user("Matt", "Delac")
greet_user("Sara", "Smith")

```

### Functions Default Arguments

```python
def display_full_name(first_name, last_name, middle_name=""):
  """Display a full name based on the first, last, and middle name"""
  if middle_name:
    full_name = first_name + " " + middle_name + " " + last_name
  else:
    full_name = first_name + " " + last_name
  
  print(full_name)

display_full_name("Samantha", "Smith", "Jane")
display_full_name("Sara", "Jones")
display_full_name("Matt", "Delac", "Lucien")

```

### Function Return

```python
def full_name(first_name, last_name, middle_name=None):
  """Generate full name from first and last name"""
  if middle_name:
    return first_name + " " + middle_name + " " + last_name
  else:
    return first_name + " " + last_name


name = full_name("John", "Doe")
print("The full name is " + name)
name = full_name("John", "Doe", "Jr.")
print("The full name is " + name)

```

## Debugging

### pdb

```python
import pdb; pdb.set_trace()
# or 
breakpoint()

```

## APIs

### Make API Request

```python
# Import requests
import requests

# Get the API response
response  = requests.get("https://jsonplaceholder.typicode.com/todos/1")

# Convert the response to JSON
todo = response.json()

print(todo)
print(todo['title'])

```

## None

### None type

```python
city = None


if city:
  print(f"The city is {city}")
else:
  print("The city doesn't not exist")

```

## Object-oriented Programming

### Class Initiliazer

```python
class User:
  """Defines a User class"""
  
  def __init__(self):
    """Initializes a new user"""
    print("Hello from the User class")


matt = User()
emilie =  User()
maria = User()

```

### Class Attributes and Methods

```python
class Dog:
  def __init__(self, name, age):
    """Initiaze the dog"""
    self.name = name
    self.age = age
    self.healthy = True
  
  def say_hello(self):
    """Say hello with the dog name"""
    print(f"Hello, I'm a dog named {self.name}")
    print(f"I'm {self.age} years old")

  def get_older(self):
    self.age = self.age + 1

  def rename(self, new_name):
    self.name = new_name

  def is_sick(self):
    self.healthy = False

  def is_healthy(self):
    self.healthy = True


snoopy = Dog("Snoopy", 2)
snoopy.say_hello()
snoopy.get_older()
snoopy.rename("Jimmy")
snoopy.say_hello()
snoopy.is_sick()
print(snoopy.healthy)

```

### Class logic

```python
class Dog:
  """Define a dog"""
  
  def __init__(self, name, age = 0):
    """ Initialize a dog with name and age """
    self.name = name
    self.age = age

  def greet(self):
    """ Return a dog greeting """
    return f"Hello, I'm a {self.casual_name()} named {self.name}"


  def casual_name(self):
    """ Determine the dog name based on the age"""
    if self.age < 2:
      return "puppy"
    elif self.age < 10:
      return "grown up dog"
    else:
      return "old dog"
    
    
snoopy = Dog("Snoopy")
print(snoopy.greet())

```

### Import a Python Class

```python
# main.py
from dog import Dog
from cat import Cat

snoopy = Dog("Snoopy")
print(snoopy.greet())

jimmy = Cat("Jimmy")
print(jimmy.greet())

# cat.py
class Cat:
  def __init__(self, name):
    self.name = name

  def greet(self):
    return f"Meow from {self.name}"

# dog.py
class Dog:
  def __init__(self, name):
    self.name = name

  def greet(self):
    return f"Wof from {self.name}"

```

### Class Inheritance

```python
class Animal():
    def __init__(self, name, age):
        self.name = name
        self.age = age 

    def speak(self):
        print("I am", self.name, "and I am", self.age, "years old")


class Dog(Animal):
    def __init__(self, name, age):
        self.name = name
        self.age = age
        self.type = "dog"

    # Since we inherit from the animal class we can use the method speak on Dog objects


tim = Dog("Tim", 5)
tim.speak() # This will print "I am Tim and I am 5 years old"

```

## File Manipulation

### Read File

```python
# Open the file
file = open('cities.txt', 'r')
cities = file.readlines()

# or more Pythony approach
with open('cities.txt', 'r') as file:
  lines = file.readlines()

# loop all the cities
for city in cities:
  print(f"I want to visit {city.strip()}")

# Close the file
file.close()

```

### Read a CSV File

```python
import csv
with open('Giants.csv', mode ='r')as file:
  csvFile = csv.reader(file)
  for lines in csvFile:
        print(lines)

```

### Write in file

```python
# Write new lines into a file
file = open('cities.txt', 'w')
file.write('Lisbon\n')
file.write('Paris\n')

file.write('New York\n')

file.close()

# Append new lines into a file
file = open('cities.txt', 'w')

file.write('Tokyo\n')
file.write('Toronto\n')
file.close()

```

### Read CSV File with DictReader

```python
import csv

# Creating the raw data
cities = [
  {"country": "France", "city": "Paris", "weather": 24},
  {"country": "Portugal", "city": "Lisbon", "weather": 30},
  {"country": "Australia", "city": "Canberra", "weather": 20} 
]

# Storing the csv file field names
field_names = ['country', 'city', 'weather']

# Storing the file name we want to create
file_name = 'cities.csv'

# Create the file
with open(file_name, 'w') as csvfile:
  # Create the writer
  writer = csv.DictWriter(csvfile, fieldnames=field_names)
  # Write the file header
  writer.writeheader()
  # Write the file rows
  writer.writerows(cities)

# Open the file
with open(file_name, 'r') as csvfile:
  # Create the reader
  reader = csv.DictReader(csvfile)
  # Reader each line one by one
  for line in reader:
    print(line['country'])
    print(line['city'])
    print(line['weather'])

```

## Exception handling

### Catch Exception

```python
try:
  file = open('cities.txt', 'r')

  content = files.read()
except FileNotFoundError:
  print("cannot find the file")

try: 
  12 / 0
except ZeroDivisionError:
  print('cannot divide number by 0')

try: 
  a + b
except Exception:
  print('something went wrong')

print("hello world")

```
