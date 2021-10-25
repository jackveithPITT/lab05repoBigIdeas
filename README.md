# Lab 5
This program was created by Jack Veith and Camryn Simons

# General overview
The program takes the input of someone's name, their favorite number, combines the two input strings together, and then hashes that string as the output.

# Specifics

```python
import hashlib
```

The program imports *hashlib* for the ability to use *sha256* to hash the string.

```python
name = input("what is your name?")
```
Then, the program prompts the user for the input of a name with the string "What is your name?"

The program then asks the user to input their favorite number within a try-except block, to ensure that the user actually enters a number. The string is then hashed using *sha256* and prints.

```python
try:
    num = int(input(name + ", what is your most favorite number?"))
    
    string = name + str(num)

    print("the SHA256 hash of " + string + " is: " + hashlib.sha256(string.encode()).hexdigest())
except:
    print("Not a Number.")
```

#License
We chose to utilize with the ISC License because it is the default license chosen by npm or the Node Package Manager. It is also stated to be equivalent to the MIT License, which is another well-known license. To boot, it is short and simple, concise and easy to understand.
