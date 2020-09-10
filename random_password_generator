#!/usr/bin/python

# python random password generator

# First we need to import the random module
import random

# Set up the password list we will use to make the password
password = []

# Ask the user how many characters long they would like the password
pwLength = int(input('How many characters long? ')) # this is to be sure it is a digit and not a string

# Then create the lists that contain the characters that will be used to make the password using all 
# four character types: uppercase letters, lowercase letters, digits, and special characters

# Make the lowercase letters list
alphaLower = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h',
              'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p',
              'q', 'r', 's', 't', 'u', 'v', 'w', 'x',
              'y', 'z']

# Make the uppercase letters. Since I lack the desire to re-type the list, I will create one based
# off the previous list
alphaUpper = [] # this set's up the list
for char in alphaLower:
    alphaUpper.append(char.upper()) # this adds the uppercase version of each list entry from alphaLower

# Now the digits:
number = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# And finally the special characters
spChar = ['.', ';', '!', '@', '#', '$', '%', '^',
          '&', '*', '(', ')', '-', '_', '=', '+',
          '<', '>', '/', '?', '~'. '[', ']', '{',
          '}']

# Create a function that randomly chooses one item from a list
def chooseOne(choice):
    return choice[random.randint(0, len(choice) - 1)]

# Let's begin the loop based on the user's input
for i in range(0, pwLength):
    # Make a pool that is restocked with randomly chosen characters from each list for each loop
    pool = [chooseOne(alphaLower), chooseOne(alphaUpper), str(chooseOne(number)), chooseOne(spChar)]
    # NOTE: In order to print the password as a string, we need to make sure the digits are converted to a string
    # or the script will not function since you cannot add together a string and a digit.
    # Choose one character from the pool and save it in a variable
    chosen = chooseOne(pool)
    # Now append that to the password list we defined at the beginning of the script
    password.append(chosen)
    
# Whew! Now that's done, let's print the list as a single string of characters by joining the list with no spaces
print(''.join(password))
