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

        - created a variable inside a function w/the same name as the global variable
        ex: x = "awesome"

            def myfunc():
            x = "fantastic"
            print("Python is " + x)

            myfunc()

            print("Python is " + x)
            # Python is fantastic
            # Python is awesome 

        - global keyword - the variable belongs to the global scope 
        ex: def myfunc():
                global x
                x = "fantastic"

            myfunc()

            print("Python is " + x)  # Python is fantastic
        
        * change a global variable inside a function 
        ex: x = "awesome"

            def myfunc():
                global x
                x = "fantastic"

            myfunc()

            print("Python is " + x)  # Python is fantastic

data types - get the data type of any object by using the type() function

numbers 
    - 3 types: int, float, complex
    - type conversion - convert from one type to another w/ the int(), float(), complex()
    - random numbers - use import random and then use random keyword to print 
    ex: import random

        print(random.randrange(1, 10)) 

casting 

len function - len() - returns the length of a string

strings:
    - not in = keywords that helps in checking certain phrases or characters is NOT present in a string
    ex: txt = "The best things in life are free!"
        print("expensive" not in txt) # True
    
    - slicing - allows you to return a range of characters
    ex: b = "Hello, World!"
        print(b[2:5]) # llo

    - modify strings
        - .upper() - returns string in upper case
        - .lower() - returns string in lower case
        - .strip() - removes any whitespace from the beginning or the end
        ex: a = " Hello, World! "
            print(a.strip()) # Hello, World!
        - .split() - returns a list where the text between the specified separator becomes the list items
        ex: a = "Hello, World!"
            b = a.split(",")
            print(b) # ['Hello', 'World!']
    
    - concatenate strings - w/ (+) sign

    - format() - takes passed arguments, formats them, and places them in the string where the placeholders {} are
    ex: quantity = 3
        itemno = 567
        price = 49.95
        myorder = "I want {} pieces of item {} for {} dollars."
        print(myorder.format(quantity, itemno, price)) 

    ex: quantity = 3
        itemno = 567
        price = 49.95
        myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
        print(myorder.format(quantity, itemno, price)) 

    - escape characters - use \ \ around text that you want to use quotes for 
    ex: txt = "We are the so-called "Vikings" from the north."
        txt = "We are the so-called \"Vikings\" from the north." 
        # We are the so-called "Vikings" from the north.
    
booleans: same as other languages

operators:
    - and - keyword
    - or - keyword
    - not - keyword
    - % - modulus
    - ** - exponentiation
    - // - floor division

lists - used to store multiple items in a single variable + store collections of data



        
        