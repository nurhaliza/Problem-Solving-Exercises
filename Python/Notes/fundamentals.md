Reference: https://www.w3schools.com/python/default.asp 

basic rules:
(#) - used for single-line comment(s)
""" """ - used for multi-line comments
indentation is key - since no semi-colons are used to end/complete lines of code

variables:
    = containers for storing data values
    - has no command for declaring a variable, variable is created the moment a value is assigned to it
    ex: x = 5 # num type
        y = "John" # string type

    - casting = specify the data type of a variable - is possible
    ex: x = string(3) # 3
        y = int(3)    # 3
        z = float(3)  # 3.0

    - variables names have the following rules:
        - must start with a letter or underscore character
        - cannot start with a number 
        - can contain only alpha-numeric characters and underscores (A-z), (0-9), _
        - case-sensitve 

    - assign multiple values
        - many values to multiple variables
        ex: x, y, z = "Orange", "Banana", "Cherry"
            print(x) # Orange
            print(y) # Banana 
            print(z) # Cherry

        - one value to multiple variables
        ex: x = y = z = "Orange"
            print(x) # Orange
            print(y) # Orange
            print(z) # Orange

        - unpack a collection - collection of values in a list, tuple, etc. can extract values into variables
        ex: fruits = ["Apple", "Banana", "Cherry"]
            x, y, z = fruits
            print(x) # Apple
            print(y) # Banana
            print(z) # Cherry

    - output variables - print() function
        - output multiple variables 
        ex: w/commas
            x = "Python"
            y = "is"
            z = "awesome"
            print(x, y, z)
            # Python is awesome

        ex: w/(+) operator - spaces are used after the word to produce the expected outcome
        * cannot use this for joining different variables
            x = "Python "
            y = "is "
            z = "awesome"
            print(x + y + z)
            # Python is awesome

    - global variables - created outside the function, can be used by everyone both inside and outside the function  
    ex: x = "awesome"

        def myfunc():
        print("Python is " + x)

        myfunc()  # Python is awesome