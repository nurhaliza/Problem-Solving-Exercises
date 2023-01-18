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

lists: - used to store multiple items in a single variable/store collections of data
      - ordered (defined order), changeable (can change, add and remove items in a list after it has been created), and allow duplicate values
      - if you add new items to a list, the new items will be placed at then end of the list
      - are indexed and can have items with the same value
      - mutable
      - ways to use lists:

        - access items - by referring to the index number
            ex: thislist = ["apple", "banana", "cherry"]
                print(thislist[1]) # banana
            - negative indexing
            ex: thislist = ["apple", "banana", "cherry"]
                print(thislist[-1]) # cherry 
            - range of indexes 
            ex: thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
                print(thislist[2:5]) # ['cherry', 'orange', 'kiwi']
            ex: thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
                print(thislist[:4]) # ['apple', 'banana', 'cherry', 'orange'] 
            ex: thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
                print(thislist[2:]) # ['cherry', 'orange', 'kiwi', 'melon', 'mango']

        - change items - by referring to the index number
            - replacing values in a list
            ex: thislist = ["apple", "banana", "cherry"]
            thislist[1] = "blackcurrant"
            print(thislist) # ['apple', 'blackcurrant', 'cherry']
            - replacing multiple values in a list
            ex: thislist = ["apple", "banana", "cherry"]
                thislist[1:2] = ["blackcurrant", "watermelon"]
                print(thislist) # ['apple', 'blackcurrant', 'watermelon', 'cherry']
            - if you insert less items than you replace, then the new items will be inserted  where you specified
            ex: thislist = ["apple", "banana", "cherry"]
                thislist[1:3] = ["watermelon"]
                print(thislist) # ['apple', 'watermelon']

            - insert() method - insert a new list item, w/out replacing any of the existing values 
            ex: thislist = ["apple", "banana", "cherry"]
                thislist.insert(2, "watermelon")
                print(thislist) # ['apple', 'banana', 'watermelon', 'cherry']

            - append() method - to add an item to the end of the list 
            ex: thislist = ["apple", "banana", "cherry"]
                thislist.append("orange")
                print(thislist) # ['apple', 'banana', 'cherry', 'orange']

            - extend() method - adds collections of data to a list
            ex: thislist = ["apple", "banana", "cherry"]
                tropical = ["mango", "pineapple", "papaya"]
                thislist.extend(tropical)
                print(thislist) # ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
                - can append tuples, sets, dictionaries, etc.
                ex: thislist = ["apple", "banana", "cherry"]
                    thistuple = ("kiwi", "orange")
                    thislist.extend(thistuple)
                    print(thislist) # ['apple', 'banana', 'cherry', 'kiwi', 'orange']

            - remove() method - removes specified item(s)
            ex: thislist = ["apple", "banana", "cherry"]
                thislist.remove("banana")
                print(thislist) # ['apple', 'cherry']

            - pop() method - removes the specified index
            ex: thislist = ["apple", "banana", "cherry"]
                thislist.pop(1)
                print(thislist) # ['apple', 'cherry']
                - if you do not specify the index
                ex: thislist = ["apple", "banana", "cherry"]
                    thislist.pop()
                    print(thislist) # ['apple', 'banana']

            - del keyword removes specified index
            ex: thislist = ["apple", "banana", "cherry"]
                del thislist[0]
                print(thislist)
                - delete entire list
                ex: thislist = ["apple", "banana", "cherry"]
                    del thislist

            - clear() method - empties the list
            ex: thislist = ["apple", "banana", "cherry"]
                thislist.clear()
                print(thislist) # []

        - loops
            - for loop - used when # of iterations is known
            ex: thislist = ["apple", "banana", "cherry"]
                for x in thislist:
                print(x)
                - loop through by index numbers 
                ex: thislist = ["apple", "banana", "cherry"]
                    for i in range(len(thislist)):
                    print(thislist[i])

            - while loop - used when execution is done until statement in program is proved wrong
            # using len() function to determine the length of the list 
            ex: thislist = ["apple", "banana", "cherry"]
                i = 0
                while i < len(thislist):
                print(thislist[i])
                i = i + 1
                # apple banana cherry

            - list comprehension - create a new list based on the values of an existing list 
            ex: thislist = ["apple", "banana", "cherry"]
                [print(x) for x in thislist]
                - with for loop in use:
                ex: fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
                    newlist = []

                    for x in fruits:
                    if "a" in x:
                        newlist.append(x)

                    print(newlist)
                - with list comprehension in use:
                ex: fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

                    newlist = [x for x in fruits if "a" in x]

                    print(newlist)
                - to replace value in list
                ex: fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
                    newlist = [x if x != "banana" else "orange" for x in fruits]

        - sorting lists
            - alphanumerically - using sort() method 
            ex: # ascending
                thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
                thislist.sort()
                print(thislist)
            ex: # descending
                thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
                thislist.sort(reverse = True)
                print(thislist)

            - sort list - reverse order by the reverse() method 
            ex: thislist = ["banana", "Orange", "Kiwi", "cherry"]
                thislist.reverse()
                print(thislist) # ['cherry', 'Kiwi', 'Orange', 'banana']

        - copy a list - using copy() method or list() method
        ex: # using copy()
            thislist = ["apple", "banana", "cherry"]
            mylist = thislist.copy()
            print(mylist) # ['apple', 'banana', 'cherry']
        ex: # using list()
            thislist = ["apple", "banana", "cherry"]
            mylist = list(thislist)
            print(mylist) # ['apple', 'banana', 'cherry']

        - join lists 
            - (+) operator 
            ex: list1 = ["a", "b", "c"]
                list2 = [1, 2, 3]

                list3 = list1 + list2
                print(list3) # ['a', 'b', 'c', 1, 2, 3]
            - append() method
            ex: list1 = ["a", "b" , "c"]
                list2 = [1, 2, 3]

                for x in list2:
                list1.append(x)

                print(list1) # ['a', 'b', 'c', 1, 2, 3]
            - extend() method 
            ex: list1 = ["a", "b" , "c"]
                list2 = [1, 2, 3]

                list1.extend(list2)
                print(list1) # ['a', 'b', 'c', 1, 2, 3]

tuples: - used to store multiple items in a single variable
        - collection that is ordered, immutable/unchangeable (cannot change, add, or remove items once tuple is created), allows duplicate values 
        - indexed
        ex: thistuple = ("apple", "banana", "cherry")
            print(thistuple) # ('apple', 'banana', 'cherry')
        ex: thistuple = ("apple", "banana", "cherry", "apple", "cherry")
            print(thistuple) # ('apple', 'banana', 'cherry', 'apple', 'cherry')

        - access items - refer items
        ex: thistuple = ("apple", "banana", "cherry")
            print(thistuple[1]) # banana
        ex: # negative indexing
            thistuple = ("apple", "banana", "cherry")
            print(thistuple[-1]) # cherry

        - range of indexes
        # positive indexes
        ex: thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
            print(thistuple[:4]) # ('apple', 'banana', 'cherry', 'orange')
        ex: thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
            print(thistuple[2:]) # ('cherry', 'orange', 'kiwi', 'melon', 'mango')
        # negative indexes
        ex: thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
            print(thistuple[-4:-1]) # ('orange', 'kiwi', 'melon')
        
        - checking values
        ex: thistuple = ("apple", "banana", "cherry")
            if "apple" in thistuple:
            print("Yes, 'apple' is in the fruits tuple") # Yes, 'apple' is in the fruits tuple
        
        - changing values 
            - convert tuple into a list or add tuples together 
            - use del keyword to complete delete tuple

        - unpacking a tuple
            - packing a tuple = assigning values to it
            - to unpack - can extract values back into variables
            ex: fruits = ("apple", "banana", "cherry")

                (green, yellow, red) = fruits

                print(green)
                print(yellow)
                print(red)
            - using the asterick (*) allows for values to be assigned to a variable as a LIST
            ex: fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")

                (green, yellow, *red) = fruits

                print(green)
                print(yellow)
                print(red)
                """
                apple
                banana
                ['cherry', 'strawberry', 'raspberry']
                """
        
        - looping + joining tuples - similar to lists



                            


        
        