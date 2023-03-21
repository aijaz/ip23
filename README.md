# ip23

# Syllabus & Lesson Plan

This class is based on [Python Crash Course, 3rd Edition](https://nostarch.com/python-crash-course-3rd-edition/) as the course textbook. The syllabus (mostly) follows the order of topics as introduced in the book. I will be using different examples during class so you can use the book to study the topics in greater detail, and get a better understanding of them.

## Week 1
* Welcome
    - About me
    - About MYPI
        + Two sisters
        + Originally for girls
        + I do outdoor stuff and am also Director of Technology
    - What you'll learn in this class
        + Programming with Python
        + Good enough to interview
* House Rules
    - Feel free to interrupt
        + Just unmute yourself
        + Or raise your hand
    - I'll feel free to tell you to hold on
    - It's ok to say I don't understand 
        + That's on me, not on you
        + Different ways to explain work with different people
    - It's up to you if you want to turn your video on or not
        + It's easier for me to judge if you're confused about something if your video is on. 
        + But at the end it's up to you, and I won't be offended one way or the other
    - Office hours
* Computers are stupid
    * Order
    * Explicit instructions 
    * Only understand very simple languages
* Launching and using the REPL
    * Your first Python Program in the repl
    * Print("hello world")
    * Now you're a programmer
* Pycharm
    * Launch
    * Creating a new project.
    * Type in hello_world.py 
    * How to run the current file
    * Add a second print statement 
* What happens when you run a program
* Syntax highlighting

## Week 2

* Variables
    * Use a sheet of paper, folded up
    * Two sheets. Give a sheet to each student
    * Ask student to unfold and read the value
    * Use wrong name: Computers are stupid
    * Update variable repeat
    * Message = "hw" print message 
    * Try invalid variable names
        * starting with number
        * With space
        * Typos
    * Assignment 
    * Lookup
    * Give a student a blank sheet. None.
    * Multiple assignment
* Strings
* Operators 
    * print "hello " + "world" string
    * Introduce Integers
    * Int operators
* Functions - title(), upper(), and lower()
* Use pycharm
* "Hello world".title()
* Using variables in strings: f strings
* New lines in strings
* Quotes in strings
* Double and triple quoted strings 
* Comments 
    * why use comments?
* Reading User Input 
* Putting it all together

    ```python
    name = input("What is your name? ")
    print("Hello " + name + "!")
    print(f"Hi there, {name}!")
    ```

* **Homework**
    * Babyshark.py
    * Write a program that asks you to input a string. Once you input a string it should print out that string, followed by "shark! Do do do, do do do!" 3 times followed by the string, and then "shark"

    ```
        What is your name? 
        Baby
        Baby shark! Do do do do do do!
        Baby shark! Do do do do do do!
        Baby shark! Do do do do do do!
        BABY SHARK!
    ```
    
* Homework answer

    ```python
    name = input("What is your name? ")
    print(name + " shark! Do do do do do do!")
    print(name + " shark! Do do do do do do!")
    print(name + " shark! Do do do do do do!")
    print(name.upper() + " SHARK!")    
    ```

## Week 3: Introduction to Lists and Tuples

- Anything we missed last week

* What is a list
* Accessing elements with indexes
    * index 0 refers to the first item in the list
    * It's this way in most computer languages
    * Think of an index as the _distance from the first item_
    * The index of the last item is the length of the list - 1

        ```python
        my_list = [10, 20, 30]
        l = len(my_list)
        my_list[0]
        my_list[1]
        my_list[2]
        my_list[3] # this should throw an error. Talk about this
        ```

    * You can also use negative indexes. `-1` for the last item, and so on
    * `li = things[-1]`
    * Why `-1`?  Because `-0` doesn't make sense.
* Changing, adding, and removing elements
    * modifying elements 
    * Adding elements `append`
    * `insert(0, "abc")`
    * `l = things.pop()`
    * `a = things.pop(3)`
    * `things.del(3)`
    * `things.remove('a thing')`
    * `l1.extend(l2)` 
* Organizing a list
    * Sort permanently with `cars.sort()`
    * Get a sorted copy with `sorted(cars)`
    * Reversing a list with `cars.reverse()`
* `n = len(things)` 
* Tuples
    * Parens 
    * Safety check
    * Usually heterogenous
    
### Week 3 class notes:

```python
a = 5
print(a)

l = ['Bulls', 'Nuggets', 'Aijaz', 42, '😃']
print(l)

m = "['Bulls', 'Nuggets', 'Aijaz', 42, '😃']"
print(m)

print(l[3])
print(m[3])

print(random.choice(l))

print(random.choice(['Heads', 'Tails']))
print(random.choice(['Blue', 'Green']))


l = ['Bulls', 'Nuggets', 'Aijaz', 42, '😃😊']
print(l[0])
print(len(l))
print(l[len(l) - 1])
print(l[-1])
print(l[-3])
print(l[-5])

print(len("Aijaz"))
print("Aijaz".upper())

# len() or print() or blahBlahBlah()
# 'global' functions that can take different kinds of parameters

# a.blah() or a.upper() or a.yadaYada()
# blah(a) or upper(a) or yadaYada(a) IF SUCH A THING EXISTED

print(len(l))
print(l)
l.append(3.14) # Think of it as append(l, 3.14)
print(l)
l.pop()
print(l)

students = ['Aijaz', 'Yasin', 'Abdallah', 'Aijaz']
students.append('Dawood')
print(students)
# removed = students.pop(2)
# print(removed)
students.remove('Aijaz')
print(students)

my_kids = []
my_kids.append('Maazin')
print(my_kids)
my_kids.append('Muneeb')
print(my_kids)

print(l)
print(students)
l.extend(students)
print(l)
l.remove(42)
l.remove('😃😊')
print(l)
# l.sort(reverse=True)
# print(l)
l.append('Jojo')
l.append('Hidyatullah')
l.append('Bilal')
l.append('AbdurRahman')
print(l)
print(sorted(l))
print(l)
# l.sort(key=lambda x: (len(x), not x))
print(sorted(sorted(l, reverse=True), key=len))
```
    
## Week 4 List References:

* List copy references 
    * References
    * Make a "book" of folded sheets of paper
    * Have one student "hold" it with a string
    * Have another student hold onto it as well
    * Update the value in one of the folded sheets 
    * Ask each student to read out their value written on the paper
    * Explain that the strings are references and that the students are variables
    * Making a copy with `l2 = list(l1)`
    * Get a second blank book and copy the values from one book to another
    * Repeat the exercise with lists of lists (books containing books)
    
* **Week 4 Homework**

3-4. Guest List:

If you could invite anyone, living or deceased, to dinner, who would you invite? Make a list that includes at least three people you’d like to invite to dinner. Then use your list to print a message to each person, inviting them to dinner. 

3-5. Changing Guest List: You just heard that one of your guests can’t make the dinner, so you need to send out a new set of invitations. You’ll have to think of someone else to invite. 

- Start with your program from Exercise 3-4. Add a print() call at the end of your program, stating the name of the guest who can’t make it. 
- Modify your list, replacing the name of the guest who can’t make it with the name of the new person you are inviting.
- Print a second set of invitation messages, one for each person who is still in your list. 

3-6. More Guests: You just found a bigger dinner table, so now more space is available. Think of three more guests to invite to dinner. 

Start with your program from Exercise 3-4 or 3-5. Add a print() call to the end of your program, informing people that you found a bigger table. 

- Use insert() to add one new guest to the beginning of your list. 
- Use insert() to add one new guest to the middle of your list. 
- Use append() to add one new guest to the end of your list. 
- Print a new set of invitation messages, one for each person in your list.

3-7. Shrinking Guest List: You just found out that your new dinner table won’t arrive in time for the dinner, and now you have space for only two guests. 

- Start with your program from Exercise 3-6. Add a new line that prints a message saying that you can invite only two people for dinner. 
- Use pop() to remove guests from your list one at a time until only two names remain in your list. Each time you pop a name from your list, print a message to that person letting them know you’re sorry you can’t invite them to dinner. 
- Print a message to each of the two people still on your list, letting them know they’re still invited. 
- Use del to remove the last two names from your list, so you have an empty list. Print your list to make sure you actually have an empty list at the end of your program.

3-8. Seeing the World: Think of at least five places in the world you’d like to visit. 

- Store the locations in a list. Make sure the list is not in alphabetical order. 
- Print your list in its original order. Don’t worry about printing the list neatly; just print it as a raw Python list. 
- Use sorted() to print your list in alphabetical order without modifying the actual list. 
- Show that your list is still in its original order by printing it. 
- Use sorted() to print your list in reverse-alphabetical order without changing the order of the original list. 
- Show that your list is still in its original order by printing it again. 
- Use reverse() to change the order of your list. Print the list to show that its order has changed. 
- Use reverse() to change the order of your list again. Print the list to show it’s back to its original order.
- Use sort() to change your list so it’s stored in alphabetical order. Print the list to show that its order has been changed. 
- Use sort() to change your list so it’s stored in reverse-alphabetical order. Print the list to show that its order has changed. 


3-9. Dinner Guests: Working with one of the programs from Exercises 3-4 through 3-7, use len() to print a message indicating the number of people you’re inviting to dinner.

    
## Week 5 Homework Review:

### Week 5 Notes:

```python
# If you could invite anyone, living or deceased, to dinner,
# who would you invite? Make a list that includes at least
# three people you’d like to invite to dinner. Then use your
# list to print a message to each person, inviting them to dinner.

guests = ['A', 'B', 'C']
print(f"Hello, {guests[0]}. Please join me for dinner.")
print("Hello, " + guests[1] + ". Please join me for dinner.")
print(f"Hello, {guests[2]}. Please join me for dinner.")


# 3-5. Changing Guest List: You just heard that one of your guests can’t make the dinner,
# so you need to send out a new set of invitations. You’ll have to think of someone else to invite.

# - Start with your program from Exercise 3-4. Add a print() call at the end of your program,
#   stating the name of the guest who can’t make it.
print(f"Oh no! {guests[1]} can't make it!")

# - Modify your list, replacing the name of the guest who can’t make it with the
#   name of the new person you are inviting.
guests[1] = 'D'

# - Print a second set of invitation messages, one for each person who is still in your list.
print(f"Hello, {guests[0]}. Please join me for dinner.")
print("Hello, " + guests[1] + ". Please join me for dinner.")
print(f"Hello, {guests[2]}. Please join me for dinner.")

# 3-6. More Guests: You just found a bigger dinner table, so
# now more space is available. Think of three more guests to
# invite to dinner.

# Start with your program from Exercise 3-4 or 3-5. Add a print()
# call to the end of your program, informing people that you found a bigger table.

print("I found a bigger table!")

#
# - Use insert() to add one new guest to the beginning of your list.
guests.insert(0, 'E')

# [E, A, D, C]
# - Use insert() to add one new guest to the middle of your list.
guests.insert(2, 'F')

# [E, A, F, D, C]
# - Use append() to add one new guest to the end of your list.

guests.append('G')

# [E, A, F, D, C, G]
# - Print a new set of invitation messages, one for each person in your list.
print(f"Hello, {guests[0]}. Please join me for dinner.")
print("Hello, " + guests[1] + ". Please join me for dinner.")
print(f"Hello, {guests[2]}. Please join me for dinner.")
print(f"Hello, {guests[3]}. Please join me for dinner.")
print(f"Hello, {guests[4]}. Please join me for dinner.")
print(f"Hello, {guests[5]}. Please join me for dinner.")


# 3-7. Shrinking Guest List: You just found out that your new dinner table
# won’t arrive in time for the dinner, and now you have space for only two guests.

# - Start with your program from Exercise 3-6. Add a new line that prints a message
# saying that you can invite only two people for dinner.

print("I'm so sorry! I can only invite 2 people for dinner")

# - Use pop() to remove guests from your list one at a time
# until only two names remain in your list. Each time you pop
# a name from your list, print a message to that person letting
# them know you’re sorry you can’t invite them to dinner.
disinvited = guests.pop()
print(f"I'm so sorry, {disinvited}. I don't have room for you at dinner.")
disinvited = guests.pop()
print(f"I'm so sorry, {disinvited}. I don't have room for you at dinner.")
disinvited = guests.pop()
print(f"I'm so sorry, {disinvited}. I don't have room for you at dinner.")
disinvited = guests.pop()
print(f"I'm so sorry, {disinvited}. I don't have room for you at dinner.")

# - Print a message to each of the two people still on your list,
# letting them know they’re still invited.

print(f"Hey, {guests[0]}. You are still invited.")
print(f"Hey, {guests[1]}. You are still invited.")

# - Use del to remove the last two names from your list,
# so you have an empty list. Print your list to make sure
# you actually have an empty list at the end of your program.

# [E A]


del(guests[0])  # [A]
del(guests[0])  # []

print(guests)


# 3-8. Seeing the World: Think of at least five places in the world you’d like to visit.

# - Store the locations in a list. Make sure the list is not in alphabetical order.
locations = ['H', 'X', 'C', 'A', 'W']

# - Print your list in its original order. Don’t worry
# about printing the list neatly; just print it as a raw Python list.
print(locations)

# - Use sorted() to print your list in alphabetical order without modifying the actual list.
print(sorted(locations))
# l2 = sorted(locations)
# print(l2)

# - Show that your list is still in its original order by printing it.
print(locations)

# - Use sorted() to print your list in reverse-alphabetical order without
# changing the order of the original list.
print(sorted(locations, reverse=True))
# l2 = sorted(locations, reverse=True)
# print(l2)

# - Show that your list is still in its original order by printing it again.
print(locations)

# - Use reverse() to change the order of your list. Print the list to show that its order has changed.
locations.reverse()
print(locations)

# - Use reverse() to change the order of your list again.
# Print the list to show it’s back to its original order.
x = locations.reverse()
print(locations)

# - Use sort() to change your list so it’s stored in alphabetical order.
# Print the list to show that its order has been changed.
locations.sort()
print(locations)

# - Use sort() to change your list so it’s stored in reverse-alphabetical order.
# Print the list to show that its order has changed.
locations.sort(reverse=True)
print(locations)

kids = []
kids.append('Maazin')
kids.append('Muneeb')
kids.append('Noor')
kids.append('Naadir')

l = sorted(kids)
print(kids)
print(l)

l[3] = 'Nour'
print(kids)
print(l)

kids.sort()

print(kids)
print(l)

kids.append("Nosey")
print(kids)

# 1. Make a list of your favorite sports in order of preference (most favorite first)
# 2. Print the list
# 3. You learn about a new game called "7 tiles" and suddenly it's your favorite game.
#    Modify the list so that this is new game is now in the first spot, with everything
#    else moving down a spot. Print the list.
# 4. After a week, "7 tiles" moves to the second spot but the third most favorite game
#    moves to the top spot. Modify the list accordingly, and print the list.
# 5. After another week, you get bored of "7 tiles" and remove it from your list
#    altogether. Everything else stays the same. Modify the list accordingly, and print the list.
# 6. Print the list in reverse order

sports = ['Snowboarding', 'Soccer', 'Cricket', 'Basketball', 'Baseball']
print(sports)
sports.insert(0, '7 tiles')
print(sports)
third = sports.pop(2)
sports.insert(0, third)
print(sports)
sports.pop(1)
print(sports)
sports.reverse()
print(sports)
exp = sports.reverse()
print(exp)
extreme_sports = list(sports)
extreme_sports[0] = 'Motocross'
print(sports)
print(extreme_sports)
l = list(sports)
l.reverse()
print(l)
l2 = sports.copy()
l2 = sports[:]

```

## Week 6: Iteration

```python
comic_books = ['Tintin', 'Asterix', 'Avatar', 'Nimona', 'The Far Side', 'Calvin and Hobbes']
print("I have Tintin comic books on the first shelf of my bookshelf")
print("I have Asterix comic books on the first shelf my bookshelf")
print("I have Avatar comic books on the firsr shelf of my bookshelf")
print("I have Nimona comic books on the first shelf of my bookshelf")
print("I have The Far Side comic books on rht first shelf of  on my bookshelf")
print("I have Calvin and Hobbes comic books on the first shelf of my bookshelf")

comic_books = ['Tintin', 'Asterix', 'Avatar', 'Nimona', 'The Far Side', 'Calvin and Hobbes']
for book in comic_books:
    print(f"I have {book} comic books on the second shelf of my bookshelf")

"""
Oh, I see that I need to iterate over the list named comic_books
I will use a variable named 'book' to refer to the current book inside the comic_books list
What should I do over and over again? Anything that is indented 4 spaces
Let's start.

book = 'Tintin'
print(f"I have {book} comic books on my bookshelf")
book = 'Asterix'
print(f"I have {book} comic books on my bookshelf")
book = 'Avatar'
print(f"I have {book} comic books on my bookshelf")
book = 'Nimona'
print(f"I have {book} comic books on my bookshelf")
book = 'The Far Side'
print(f"I have {book} comic books on my bookshelf")
book = 'Calvin and Hobbes'
print(f"I have {book} comic books on my bookshelf")
# Is there anything after Calvin and Hobbes? No. Okay then. We're done.
"""

# comic_books is known as an "Iterable" because you can iterate over it.
for number in (2, 4, 6, 8, 10, 12, 14, 16, 18, 20):
    print(f"{number} is an even number. It is divisible by 2")


name = "Sulaiman"
for letter in name:
    print(letter)


for letter in "Hwek@$#@12..#$":
    print(letter)


# Talk about indentation.


comic_books = ['Tintin', 'Asterix', 'Avatar', 'Nimona', 'The Far Side', 'Calvin and Hobbes']
for book in comic_books:
    print(f"I have {book} comic books on the second shelf of my bookshelf")

print("I like this comic book")


for person in ("Aijaz", "Adel", "Ayesha"):
    print(f"Hello, {person}")

print("It's good to meet all of you.")

total = 0
for number in (2, 4, 6, 8, 10):
    total = total + number
    print(f"{number} is an even number. It is divisible by 2")

print(f"The sum of the first 5 even numbers is {total}")

"""
total = 0
total = total + 2
print(...)
total = total + 4
print(...)
total = total + 6
print(...)
total = total + 8
print(...)
total = total + 10
print(...)

print("... total")
"""

total = 0
for n in range(1, 101):
    total = total + n

print(f"The sum of the first 100 numbers is {total}")

for n in range(5):  # the same as for n in range(0, 5) - which is the same as for n in (0, 1, 2, 3, 4)
    print(n)

for n in range(0, 10, 2):
    print(n)

total = 0
for n in range(1, 1000000, 2):
    total = total + n

print(total)

for n in range(0, 10, 2):
    print(n)

# for n in [0, 2, 4, 6, 8, 10, 12, ... 999998]:
#     print(n)

print([0, 2, 4, 6, 8])
print(range(0, 10, 2))

r = range(0, 1000000000, 2)
print(r)

total = 0
for n in r:
    total = total + n

print(total)

```

* Lists containing lists
    * `l1.append(l2)`
    * List data structures
        * [x,y]
        * If you never need to add or delete, use tuples instead 

### Week 6 Homework

I'm creating an Avatar Fandom page. I want to keep track of the following information for each character: Name, Nationality, Children, Bending. 

- Every character will have a name and nationality
- We will keep track of the names of the character's children (if any)
- Some characters may not have children
- Some characters will have a single bending power
- Some characters will have more than one bending power
- Some characters may not have any bending powers
- Design a data structure for this fandom page
- Populate your data structure using the data below
- Print the value of your data structure
- This is gonna take some thought, so spend some time on this assignment.

Data:

+ Name: Aang
    + Nationality: Southern Air Temple
    + Children: 
        * Bumi
        * Kya
        * Tenzin
    + Bending: 
        * Air
        * Water
        * Earth
        * Fire
        * Energy
- Name: Katara
    + Nationality: Southern Water Tribe
    + Children:
        * Bumi
        * Kya
        * Tenzin
    + Bending: 
        * Water
        * Blood
- Name: Sokka
    + Nationality: Southern Water Tribe
    + Children: None
    + Bending: None
- Name: Toph Beifong
    + Nationality: Gaoling, Earth Kingdom
    + Children: 
        * Lin Beifong
        * Suyin Beifong
    + Bending:
        * Earth
        * Metal
- Name: Zuko
    + Nationality: Fire Nation Capital, Fire Nation
    + Children: 
        * Izumi
        * Kya
    + Bending:
        * Fire
        * Energy
- Name: Iroh
    + Nationality: Fire Nation Capital, Fire Nation
    + Children: 
        * Lu Ten
    + Bending:
        * Fire
        * Energy
- Name: Zhao
    + Nationality: Fire Nation Capital, Fire Nation
    + Children: 
        * None
    + Bending:
        * Fire


## Week 7

### Homework from week 6:

```python
characters = [
    ["Aang", "Southern Air Temple", ["Bumi", "Kya", "Tenzin"], ["Air", 'Water', 'Earth', 'Fire', 'Energy'], "He"],
    ["Katara", "Southern Water Tribe", ["Bumi", "Kya", "Tenzin"], ["Water", "Blood"], "She"],
    ["Sokka", "Southern Water Tribe", [], [], "He"],
    ["Toph Beifong", "Gaoling, Earth Kingdom", ["Lin Beifong", "Suyin Beifong"], ["Earth", "Metal"], "She"],
    ["Zuko", "Fire Nation Capital, Fire Nation", ["Izumi", "Kya"], ["Fire", "Energy"], "He"],
    ["Iroh", "Fire Nation Capital, Fire Nation", ["Lu Ten"], ["Fire", "Energy"], "He"],
    ["Zhao", "Fire Nation Capital, Fire Nation", [], ["Fire"], "He"]
]
```

* Did you use a list or a tuple for children or bending? Why?
* Looping through an entire list

    ```python
    things = ['Raindrops', 'Whiskers', 'Kettles', 'Mittens', 'Packages']
    for thing in things:
        print(thing)
    ```

* Step through loop
* Multiple statements in a block
    - 2 print statements

* Statements after a for loop

    ```python
    for person in ("Aijaz", "Adel", "Ayesha"):
        print(f"Hello, {person}")
        
    print("It's good to meet all of you.")
        
    the_sum = 0
    for n in (1, 2, 3, 4):
        the_sum = the_sum + n
        
    print(f"The sum of the first 4 integers is {the_sum}")
    ```

* Blank line optional
* Avoiding Indentation Errors
* Making Numerical Lists
    - Many reasons exist: games, measurements, etc.
    - Range
        + Two parameters: start_at and stop_before
        + Never includes the second parameter

            ```python
            s = 0
            for v in range(1, 4):
                s = s + v
            
            print(f"the sum of the first 3 integers is {s}")
            
            #################################################
            
            s = 0
            n = 4
            for v in range(1, n):
                s = s + v
            
            print(f"the sum of the first {n - 1} integers is {s}")
            
            #################################################
            
            s = 0
            n = 4
            for v in range(1, n):
                s += v
            
            print(f"the sum of the first {n - 1} integers is {s}")
            ```

        + `range` with 1 parameter

            ```python
            for n in range(5):
                print(n)
            ```

        + `range` with 1 parameter - starts at 0, stops at parameter - Works well with list indexes

            ```python
            odds = [1, 3, 5, 7, 9]
            for f in range(len(odds)):
                print(odds[f] + 1)
            ``` 

        + `range` with 3 parameter: increment by parameter 3 instead of 1

            ```python
            for v in range(1, 10, 3):
                print(v)
            ```

        + Using `range` to create lists

            ```python
            l = list(range(1, 10, 3))
            ```

* Functions on lists
    - `min()`
    - `max()`
    - `sum()`
    - `len()`

* List comprehensions
    - Elegant shorthand for the creation of a new list and a `for` loop.

        ```python
        numbers = [1, 2, 3, 4, 5]
        doubles = [x * 2 for x in numbers]
        triples = [item * 3 for item in numbers]
        halves = [item/2 for item in numbers]
        ``` 

    - You can also use ranges with list comprehensions

        ```python
        squares = [x**2 for x in range(1, 10)]
        ```

* List slices
    - A slice is like a range for lists
    - A slice returns a new list

        ```python
        months =   ['Jan', 'Feb', 'Mar', 
                    'Apr', 'May', 'Jun', 
                    'Jul', 'Aug', 'Sep', 
                    'Oct', 'Nov', 'Dec']
        first_3 = months[0:3] # ['Jan', 'Feb', 'Mar']
        q2 = months[3:6] # ['Apr', 'May', 'Jun']
        ```

    - Omitting the first parameter implies it's 0

        ```python
        months =   ['Jan', 'Feb', 'Mar', 
                    'Apr', 'May', 'Jun', 
                    'Jul', 'Aug', 'Sep', 
                    'Oct', 'Nov', 'Dec']
        first_third = months[:4] # ['Jan', 'Feb', 'Mar', 'Apr']
        ```

    - Omitting the second parameter implies it's the last index + 1

        ```python
        months =   ['Jan', 'Feb', 'Mar', 
                    'Apr', 'May', 'Jun', 
                    'Jul', 'Aug', 'Sep', 
                    'Oct', 'Nov', 'Dec']
        last_third = months[8:4] # ['Sep', 'Oct', 'Nov', 'Dec']
        ```

    - Omitting both parameter implies indexes 0 and the last index + 1

        ```python
        months =   ['Jan', 'Feb', 'Mar', 
                    'Apr', 'May', 'Jun', 
                    'Jul', 'Aug', 'Sep', 
                    'Oct', 'Nov', 'Dec']
        year = months[:]
        ```

    - An index of -1 is the index of the last item
    - An index of -2 is the second-last item, and so on

        ```python
        months =   ['Jan', 'Feb', 'Mar', 
                    'Apr', 'May', 'Jun', 
                    'Jul', 'Aug', 'Sep', 
                    'Oct', 'Nov', 'Dec']
        p4 = months[-4:-1] # ['Sep', 'Oct', 'Nov']
        ```

### Notes from Week 7's class

```python
print(len(characters))
print(characters[2][1])
print(characters[3][2][0])
print(len(characters[4][3]))

for character in characters:
    print(f"{character[0]} is from {character[1]}. {character[4]} has the following children: {character[2]} and bending powers: {character[3]}")

for letter in "Aijaz":
    print("The letter is " + letter)

print(len(characters))
print(len("Aijaz"))
for c in characters:
    print(f"{c[0]} has {len(c[0])} characters in their name")

numbers = [3, 2, 7, -3, 6, 2, 9, 5, 0, 6, 8]
print(max(numbers))
print(min(numbers))
print(sum(numbers))
print(sum(numbers)/len(numbers))

doubles = []
for n in numbers:
    doubles.append(n * 2)
print(doubles)


new_doubles = [n * 2 for n in numbers]  # list comprehension
print(new_doubles)

print([n * 3 for n in numbers])
print([n ** 4 for n in numbers])

months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
print(months)
print(months[0:6])  # slice
print(months[6:12])
print(months)
print(months[:3])
print(months[9:])
print(months[3:6])
print(months[6:9])
print("Aijaz"[1:])
print("Aijaz"[2:])
print(months[-3:])
print(months[:])
print(months[0:12:2])
print(months[::-1])
print("Aijaz"[::-1])
print(months[-4:-1])
print(months[-4:])

```

### Week 7 homework

1. Create a data structure to represent a planet and it's confirmed number of moons. Create a list of these data structures. You can find the data on [Wikipedia](https://en.wikipedia.org/wiki/Planet#Planetary_attributes)
2. Print the name of each planet along with its number of confirmed moons. 
3. Print the total number of confirmed moons in the solar system. 
4. For each of the the first 4 planets in the solar system, print the planet's name, and it's number of moons. Print the total number of moons for those 4 planets.
5. For each of the the last 3 planets in the solar system, print the planet's name, and it's number of moons. Print the total number of moons for those 3 planets.
6. Use a single Python statement no more than 80 characters long to generate a list of of the reciprocals of the first 1000 positive integers. (Remember: a positive integer is any whole number greater than 0, and the reciprocal of n is 1/n).


### Week 8: Homework review & Intro to conditionals

### Review of Week 7 homework

```python

# 6 different ways to do this homework

moons = [
    ("Mercury", 0),
    ("Venus", 0),
    ("Earth", 1),
    ("Mars", 2),
    ("Jupiter", 95),
    ("Saturn", 83),
    ("Uranus", 27),
    ("Neptune", 14),
]

moons_lol = [
    ["Mercury", 0],
    ["Venus", 0],
    ["Earth", 1],
    ["Mars", 2],
    ["Jupiter", 95],
    ["Saturn", 83],
    ["Uranus", 27],
    ["Neptune", 14],
]

moons_rev = [
    (0, "Mercury"),
    (0, "Venus"),
    (1, "Earth"),
    (2, "Mars"),
    (95, "Jupiter"),
    (83, "Saturn"),
    (27, "Uranus"),
    (14, "Neptune"),
]

moons_rev_lol = [
    [0, "Mercury"],
    [0, "Venus"],
    [1, "Earth"],
    [2, "Mars"],
    [95, "Jupiter"],
    [83, "Saturn"],
    [27, "Uranus"],
    [14, "Neptune"],
]

moons_flat = ["Mercury", 0,"Venus", 0,"Earth", 1,"Mars", 2,"Jupiter", 95,"Saturn", 83,"Uranus", 27,"Neptune", 14]

planet_names = ["mercury", "venus", "earth", "mars", "jupiter", "saturn", "uranus", "neptune"]
num_moons = [0, 0, 1, 2, 95, 83, 27, 14]

# 2 - Print the names and the number

for moon_structure in moons:
    print(f"{moon_structure[0]} has {moon_structure[1]} moons")

for moon_structure in moons_rev_lol:
    print(f"{moon_structure[1]} has {moon_structure[0]} moons")

for n in range(0, len(moons_flat), 2):  # We use the 3-parameter version of range to jump by 2, not 1
    print(f"{moons_flat[n]} has {moons_flat[n+1]} moons")

for n in range(len(planet_names)):
    print(f"{planet_names[n]} has {num_moons[n]} moons")

# If we want to append Pluto, it's easiest with our nested list structure

moons.append(["Pluto", 0])
for moon_structure in moons:
    print(f"{moon_structure[1]} has {moon_structure[0]} moons")

for n in range(len(moons)):
    print(f"{moons[n][0]} has {moons[n][1]} moons")

# We can also use enumerate to get a tuple of index, item: The parentheses are optional here.
for (n, name) in enumerate(planet_names):
    print(f"{name.upper()} has {num_moons[n]} moons")

# 3 - total number of moons

total_num_moons = 0
for moon_structure in moons:
    total_num_moons = total_num_moons + moon_structure[1]

print(total_num_moons)

# This is a lot easier for num_moons, because we simply sum that list.
# Moral of the story: Think about how your data will be used before you 
# design a data structure for it
print(sum(num_moons))


# 4  - Use a slice
total_num_moons = 0
for moon_structure in moons[:4]:
    print(f"{moon_structure[0]} has {moon_structure[1]} moons")
    total_num_moons = total_num_moons + moon_structure[1]

print(total_num_moons)

# 5  -
total_num_moons = 0
for moon_structure in moons[-3:]:
    print(f"{moon_structure[0]} has {moon_structure[1]} moons")
    total_num_moons = total_num_moons + moon_structure[1]

print(total_num_moons)


# 6 - Use a list comprehension

# The long way (wrong way for this question)
reciprocals = []
for n in range(1, 11):
    reciprocals.append(1/n)

print(reciprocals)

# The right way 
print([1/n for n in range(1, 1001)])

for x in [1, 2, 3]:
    print(x)


c2 = []
for x in [1, 2, 3]:
    c2.append(1/x)

r = range(1, 11)
print(r)

for x in range(1, 11):
    print(x)

c = [1/x for x in [1, 2, 3]]
print(1/x for x in range(1, 10))

```


### Conditionals

* Programs so far have been boring
* Programs get interesting when they examine conditions and make decisions based on the value of those conditions.

```python
a = 2 # hello
b = 3 # hello

if a == b: # hello
    print("a and b are equal") # hello
else:
    print("a and b are NOT equal")
```


# Week 9 3/19

```python
team = input("What is your favorite NBA team? ")

if team == "Bulls":
    print("They're my favorite team, too!")
    print("They're my hometown team")
elif team == "Nuggets":
    print("Now that I live in CO, I root for the Nuggets.")
elif team == "Warriors":
    print("They're exciting to watch")
else:
    print("I don't have strong feelings about them.")

print("It's been nice talking to you")
```

- A boolean value is a value that's either true or false. It can't be anything else
- A boolean expression is an expression that has a boolean value (True or False)
- An if statement has 0 or more 'elif' clauses, and 0 or 1 else clauses

### elif vs multiple ifs

```python
age = 75

if age < 3:
    print("You're a baby")
elif age < 6:
    print("You're a toddler")
elif age < 10:
    print("You're a child")
elif age < 13:
    print("You're a tween")
elif age < 20:
    print("You're a teenager")
elif age < 33:
    print("You're a youth")
elif age < 41:
    print("You're an grown up")
else:
    print("OMG! You're ancient!")


if age < 3:
    print("You're a baby")
if age < 6:
    print("You're a toddler")
if age < 10:
    print("You're a child")
if age < 13:
    print("You're a tween")
if age < 20:
    print("You're a teenager")
if age < 33:
    print("You're a youth")
if age < 41:
    print("You're an grown up")
else:
    print("OMG! You're ancient!")

age = 15

# Brittle code
if age < 3:
    print("You're a baby")
if age >= 3 and age < 6:
    print("You're a toddler")
if age >= 6 and age < 10:
    print("You're a child")
if age >= 10 and age < 13:
    print("You're a tween")
if age >= 13 and age < 20:
    print("You're a teenager")
if age >= 20 and age < 33:
    print("You're a youth")
if age >= 33 and age < 41:
    print("You're an grown up")
elif age >= 41:
    print("OMG! You're ancient!")

age = input("How old are you? ")
age = int(age)
if age < 3:
    print("You're a baby")
elif age < 6:
    print("You're a toddler")
elif age < 10:
    print("You're a child")
elif age < 13:
    print("You're a tween")
elif age < 20:
    print("You're a teenager")
elif age < 33:
    print("You're a youth")
elif age < 41:
    print("You're an grown up")
else:
    print("OMG! You're ancient!")

if age >= 18:
    print("You're old enough to vote")
else:
    print("You're not old enough to vote yet")

Be careful about mathematical vs lexical sorting!

age = input("How old are you? ")
if age < "3":
    print("You're a baby")
elif age < "6":
    print("You're a toddler")
elif age < "10":
    print("You're a child")
elif age < "13":
    print("You're a tween")
elif age < "20":
    print("You're a teenager")
elif age < "33":
    print("You're a youth")
elif age < "41":
    print("You're an grown up")
else:
    print("OMG! You're ancient!")

# You have to be careful about comparing numbers that are strings, 
# because the compare lexically, not numerically

# 1 10 100 2 20 200 3 30 300 lexical sorting
# 1 2 3 10 20 30 100 200 300 numerical sorting
```


```python
team = input("What is your favorite team? ")
if team.strip().lower() == "bulls":
    print("They're my favorite team, too!")
    print("They're my hometown team")
elif team.strip().title() == "Nuggets":
    print("Now that I live in CO, I root for the Nuggets.")
elif team.strip().upper() == "WARRIORS":
    print("They're exciting to watch")
else:
    print("I don't have strong feelings about them.")

print("It's been nice talking to you")


# nested if statements
age = input("How old are you? ")
age = int(age)
if age < 3:
    print("You're a baby")
elif age < 6:
    print("You're a toddler")
elif age < 10:
    print("You're a child")
elif age < 13:
    print("You're a tween")
elif age < 20:
    print("You're a teenager")
    if age < 18:
        print("You're not an adult")
    else:
        print("You're an adult")
elif age < 33:
    print("You're a youth")
elif age < 41:
    print("You're an grown up")
else:
    print("OMG! You're ancient!")

if age >= 18:
    print("You're old enough to vote")
else:
    print("You're not old enough to vote yet")

age = input("How old are you? ")
age = int(age)

```

## Creating Boolean expressions by joining Boolean expressions with and and or

```python
if age >= 13 and age <= 19:
    print("You're a teenager")
else:
    print("You are not a teenager")

# or
if 13 <= age <= 19:
    print("You're a teenager")
else:
    print("You are not a teenager")


age = input("How old are you? ")
age = int(age)
income = int(input("How much income did you have in 2022? "))

if age < 18 or income < 1000:
    print("You do not need to file")
else:
    print("You need to file")

if age >= 13 and age <= 19:
    print("You're a teenager")
```

```python
and AND or truth tables

a = True
b = True

print(f"{a} and {b} == {a and b}, {a} or {b} == {a or b}")

a = False
b = True

print(f"{a} and {b} == {a and b}, {a} or {b} == {a or b}")

a = True
b = False

print(f"{a} and {b} == {a and b}, {a} or {b} == {a or b}")

a = False
b = False

print(f"{a} and {b} == {a and b}, {a} or {b} == {a or b}")

a = True
b = True
c = True
d = True

if a and b and c and d:
    print("this is true")
else:
    print("This is false")

w = False
x = False
y = True
z = False

if w or x or y or z:
    print("This is true")
else:
    print("this is false")
```

### More booleans

```python
l1 = [1, 2, 3, 4, 5]
print(12 in l1)

if 12 in l1:
    print("12 is in the list")
else:
    print("12 is not in the list")


if "ja" in "Aijaz":
    print("It's a match")
else:
    print("Could not find the string")

```
