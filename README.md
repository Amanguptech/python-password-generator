# python-password-generator
you will learn how to make python password generator
import random

letters = ['a', 'b', 'c', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'n', 'o', 'p', 'q', 'r', 's', 't','u', 'v', 'w', 'x', 'y', 'z']
numbers = ['0', '1', '2', '3', '4' '5', '6', '7', '8', '9']
symbols = ['~', '!', '#', '$', '%', '^', '&', '*']

print("welcome to password generator")

nr_letters = int(input("how many letters do you want to add? "))
nr_numbers = int(input("how many numbers do you want to add "))
nr_symbols = int(input("how many symbols do you want to add "))

password = ''
for char in range(1,nr_letters+1):
    password += random.choice(letters)

for char in range(1, nr_numbers+1):
    password += random.choice(numbers)

for char in range(1, nr_symbols+1):
    password += random.choice(symbols)


random.shuffle(password)
print(password)
