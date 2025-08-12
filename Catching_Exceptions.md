**Try**: Something that might cause an exception

**Except**: Do this if there *was* an exception

**Else**: Do this if there were *no* exceptions

**Finally**: Do this *no matter what happens*


## Examples to understand better

- **Exception Handling**
```
try:
    file = open("a_file.txt")
    a_dictionary = {"key": "value"}
    print(a_dictionary["key"])
except FileNotFoundError:
    file = open("a_file.txt", "w")
    file.write("Something")
except KeyError as error_message:
    print(f"The key {error_message} does not exist.")
else:
    content = file.read()
    print(content)
finally:
    raise TypeError("This is an error that I made up.")
```

- **BMI Example**
```
height = float(input("Height: "))
weight = int(input("Weight: "))

if height > 3:
    raise ValueError("Human Height should not be over 3 meters.")

bmi = weight / height ** 2
print(bmi)
```

## Exercises

### Exercise 01:

**IndexError Handling**
- Issue 

We've got some buggy code. Try running the code. The code will crash and give you an IndexError.

This is because we're looking through the list of fruits for an index that is out of range. 

- Objective 

Use what you've learnt about exception handling to prevent the program from crashing. If the user enters something that is out of range just print a default output of "Fruit pie". 



IMPORTANT: The exception handling should NOT allow each fruit to be printed when there is an exception. e.g. it should not print out Apple pie, Pear pie and Orange pie, when there is an exception it should only print "Fruit pie". 

```
fruits = ["Apple", "Pear", "Orange"]

# Catch the exception and make sure the code runs without crashing.
def make_pie(index):
    fruit = fruits[index]
    print(fruit + " pie")

make_pie(4)
```

**Solution:**
```
fruits = ["Apple", "Pear", "Orange"]

def make_pie(index):
    try:
        fruit = fruits[index]
    except IndexError:
        print("Fruit pie")
    else:
        print(fruit + " pie")

make_pie(4)
```
