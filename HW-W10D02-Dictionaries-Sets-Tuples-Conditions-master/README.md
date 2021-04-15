### ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Python Programming


# Python Lists, Dictionaries, and Tuples

In this homework, you're going to write code for two challenge problems.

You'll practice these programming concepts we've covered in class:

* Using dictionaries to solve problems.
* Storing data in tuples, sets, and lists.

---


> **Hint:** Make sure you are printing something out with the `print` statement. Otherwise, you won't see any output from running your program!



# Code Challenges

## Problem 1: I Love You, Tuple

### Skill you're practicing: Using tuples.

You may recall tuples from your in-class lesson. Tuples are *immutable* data structures, which means they can't be changed after they're created. They are typically used to store related information that doesn't need to be changed, such as a student record or, in this case, some stats about a movie. It's your job to create some `print` statements that access the appropriate values inside each tuple to produce the expected output.


#### Starter Code

```python
# My favorite romance movies
# title, release year, runtime, tagline, main characters
romantic_movie1 = ("The Princess Bride", 1987, 98, "The story of a man and a woman who lived happily ever after.", ["Buttercup", "Westley", "Fezzik", "Inigo Montoya", "Vizzini"])
romantic_movie2 = ("Groundhog Day", 1993, 101, "He's having the day of his life… over and over again.", ["Phil Connors"])
romantic_movie3 = ("Amélie", 2001, 122, "One person can change your life forever.", ["Amélie Poulain", "Nino Quincampoix", "The Garden Gnome"])
```

#### Expected Output

```
Here are my favorite romance movies:

The Princess Bride (1987): The story of a man and a woman who lived happily ever after.

Groundhog Day (1993): He's having the day of his life...over and over again.

Amélie (2001): One person can change your life forever.
```
romantic_movie1 = ("The Princess Bride", 1987, 98, "The story of a man and a woman who lived happily ever after.", ["Buttercup", "Westley", "Fezzik", "Inigo Montoya", "Vizzini"])
romantic_movie2 = ("Groundhog Day", 1993, 101, "He's having the day of his life… over and over again.", ["Phil Connors"])
romantic_movie3 = ("Amélie", 2001, 122, "One person can change your life forever.", ["Amélie Poulain", "Nino Quincampoix", "The Garden Gnome"])


movie1=romantic_movie1[0]
movie1_Date= romantic_movie1[1]
movie1_Story=romantic_movie1[3]
print("Here are my favorite romance movies:")
print(f"{movie1} ({movie1_Date}): {movie1_Story} ")




movie2=romantic_movie2[0]
movie2_Date= romantic_movie2[1]
movieS2_Story=romantic_movie2[3]
print("Here are my favorite romance movies:")
print(f"{movie2} ({movie2_Date}): {movieS2_Story} ")



movie3=romantic_movie3[0]
movie3_Date= romantic_movie3[1]
movie3_Story=romantic_movie3[3]
print("Here are my favorite romance movies:")
print(f"{movie3}({movie3_Date}): {movie3_Story} ")




print("---------------------------------------------------- ")
**Hint:** Remember, you can access a tuple sort of like a list, with the square brackets `[]` counting from zero (e.g., the value of `romantic_movie1[0]` is `"The Princess Bride"`).

### Bonus:
Change the `print` statement's separator character to an empty string `""` instead of a space so that you can print the year as `(1987)` instead of `( 1987 )`.

---

## Problem 2: Friends, Colleagues, and Details

### Skill you're practicing: Using dictionaries, lists, and key-value pairs.

Your boss tasks you with creating a company directory. Make a list called `employees`, which will contain one dictionary per person and include the keys `name`, `age`, `department`, `phone`, and `salary`. Once you have the list of dictionaries set up, loop through the list and print out the `name`, `department`, and `phone` number of each employee. Their `age` and `salary` should remain secret!

#### Starter Code

A dictionary should be set up in the following way:

```python
{
    "name": "Ron Swanson",
    "age": 55,
    "department": "Management",
    "phone": "555-1234",
    "salary": "$87,000"
}
```

#### Expected Output

```
Ron Swanson in Management can be reached at 555-1234.
Leslie Knope in Middle Management can be reached at 555-4321.
Andy Dwyer in Shoe Shining can be reached at 555-1122.
April Ludgate in Administration can be reached at 555-3345.
```

**Hint:** Dictionaries have values that can be accessed with keys, for example, `employees["name"]`. Keys are typically strings.

---

# Python Conditionals: Practice Problems

In this homework, you're going to write code to solve a few problems.

You will practice these programming concepts we covered in class:
* Declaring and using variables.
* Using mathematical operators.
* Implementing Python conditionals: `if`, `elif`, and `else`.

---


> **Hint**: Make sure you are printing something out with the `print` statement. Otherwise, you won't see any output from running your program!


---

# Part 1: Mini-Quiz


1. True or false: An `if` statement can live without an `else` statement.
True

2. True or false: An `else` statement can live without an `if` statement.
False
3. True or false: An `elif` statement can live without an `if` statement.
False

4. True or false: An `if` + `elif` statement can live without an `else` statement.
True

5. True or false: The following statements are equivalent.
False
```python
if a == True:
```

```python
if a:
```

6. In the following code block, what prints?

```python
a = True
b = True
c = False

if a:
    print("1")

if b:
    print("2")

if c:
    print("3")

if a and b:
    print("4")

if a and c:
    print("5")

if b and c:
    print("6")

if a or b:
    print("7")

if a or c:
    print("8")

if b or c:
    print("9")
```


1
2
4
7
8
9

7. In the following code block, what prints?

```python
a = False
b = True
c = True

if a:
    print("1")
elif b:
    print("2")
elif c:
    print("3")
else:
    print("4")
```
2

---

# Part 2: Code Challenges

## Problem 1: Most Clocks Are Normal, But Some Are Cuckoo!

### Skill you're practicing: Writing conditionals.


You're making a program for your coworkers that displays a message on their desktop's idle screen. Depending on the time of day, you want to print a different quote. You'll create a variable, `time`, which has an integer value between zero and 23, representing the hour of the day in [military time](https://www.thebalancecareers.com/military-time-3356971), which is a 24-hour clock. Write a conditional statement with Python code that prints exactly one message using the following rules:

```
If the time of day is before 9 a.m. --> print the quote "Morning is wonderful. Its only drawback is that it comes at such an inconvenient time of day."

Otherwise if the time of day is before or exactly 4 p.m. --> print the quote "Working hard or hardly working?"

Otherwise, if the time of day is before 8 p.m. --> print the quote "How did it get so late so soon?"

Otherwise if the time of day is before 10 p.m. --> print the quote "A day without sunshine is like, you know, night."

Otherwise, for any time 10 p.m. or later --> print the quote "Burning the midnight oil!"
```

#### Starter Code

```python
time = 8
```



> **Hint:** Test your code with different values for time of day. Make sure you are only printing one statement, regardless of the value of `time`!

---

time = 8


if time <9:
    print("Morning is wonderful")
elif time <=16:
    print("Working hard or hardly working?")
elif time<20:
    print("Working hard or hardly working?")
elif time<22:
    print("A day without sunshine is like, you know, night")
else:
    print("Burning the midnight oil!")
## Problem 2: I Came, I 'Saur, I Conquered

### Skill you're practicing: Writing conditionals with multiple conditions.


The mighty Tyrannosaurus rex is the king of dinosaurs, and he does whatever he pleases. When he's hungry, he eats. When he's angry, he fights. When he's bored, he roars. When he's tired, he sleeps! Write a conditional statement that selects one of the following actions for T-Rex based on his current mood. T-Rex's actions are ordered by precedence:

```
If T-Rex is angry, hungry, and bored he will eat the Triceratops.
Otherwise if T-Rex is tired and hungry, he will eat the Iguanadon.
Otherwise if T-Rex is hungry and bored, he will eat the Stegasaurus.
Otherwise if T-Rex is tired, he goes to sleep.
Otherwise if T-Rex is angry and bored, he will fight with the Velociraptor.
Otherwise if T-Rex is angry or bored, he roars.
Otherwise T-Rex gives a toothy smile.
```

#### Starter Code

```python
angry = True
bored = True
hungry = False
tired = False

# Example `if` statement:
if bored:
    print("T-Rex roars! Rawr!")
```

angry = True
bored = True
hungry = False
tired = False

# Example `if` statement:
if bored and hungry:
    print("he will eat the Stegasaurus")
elif tired and hungry:
    print("he will eat the Iguanadon")
elif hungry and angry:
    print("he will eat the Triceratops")
elif tired:
    print(" he goes to sleep")
elif angry and bored:
    print("he will fight with the Velociraptor")
elif angry or bored:
    print("he roars")
else :
    print("T-Rex gives a toothy smile.")
## Celebrate!

You're all finished!

![](https://media.giphy.com/media/UkhHIZ37IDRGo/giphy.gif)