# Python Syntax Cheatsheet (basic)

`print("...");`

`myInput = input("...");`

`print("hello " + input("who are you?"));`

`#this is a comment`

`len("some string:);`

```
print("the question")
answer = input()
```
`print(type("hello"));`

```
stringIs = str(123);
print(type(stringIs));
#prints <class 'str'>
```

Concatenating a string to an int in python will not cast the int into a string, it will just fail.

```
print(float(123));
#prints 123.0
```
Anything coming from the input is a string.

6/3 will return 2.0 not 2

```
print(int(12.56));
#returns 12
print(int(154.123));
#returns 154
```
`print(int(2**3));  #returns 8`

```
print(round(8/3));
#2.6666 but it will round to 3

print(round(10/3));
#3.33333 but will round to 3

print(round(10/3, 3));
#will round to those decimal places: 3.333

print(8//3);
#2.6666 but will floor to just the int part, 2
```
```
amount = 48.34555

print(f"The amount is {amount}");
formatted_amount = "{:.2f}".format(amount); #48.34555
print(f"The amount is {formatted_amount}"); #48.35
```
```
number = input("give me a number: ");
if (int(number) > 5):
    print(">5");
else:
    print("<5");
```

```
number = input("give me a number: ");
if (int(number) > 10):
    print(">10");
elif (int(number)> 5):
    print(">5 and <10");
else:
    print("<10 and <5")
```
```
number = input("give me a number: ");
if (int(number) > 10 and int(number)%2 == 0):
    print(">10 and even");
else:
    print("<10 or >10 but odd");

#use or for and or
```

to import something, such as the random module `import random`, then use its functions with `random.whateverfunc`

For the modules, we can just name the file and import that directly, and use the things it has inside.

`random() ` --> 0 to 0.9999 float number
`ranint(1,10) ` --> 1 to 10

```
someArray = ["one", "two", "three", "four", "five"];
print(someArray[0]); #one
print(someArray[-1]) #five
```

```
someArray.append("six");
print(someArray);
```

`someArray.extend(["seve", "eight"])`

```
str = "hello how are you?"

array = str.split(" ");
print(array)
```

```
import random;

array = ["Anna","George", "Michael", "Maria"]

randomname = random.choice(array);
print(randomname)
```

```
array = [1,2,3,4,5]
array2 = [6,7,8,9,0]

both = [array, array2]
print(both) # prints [[1, 2, 3, 4, 5], [6, 7, 8, 9, 0]]

print(both[0]) # prints [1, 2, 3, 4, 5]

print(both[0][2]) # prints 3
```

```
fruits = ["apple", "manzana", "fresa"]

for fruit in fruits:
    print(fruit)
```
In the for, everything indented will be part of the loop (no {} needed, but make sure the indentation is right)

```
scores = [6,6, 10,8]

print(max(scores)) #10
```
```
for number in range(1, 15):
    print(number) #prints 1 through 14

#range with stepping
for number in range(1, 15, 2):
    print(number) #prints 1 3 5 7 9 11 13
```

```
def myFunc():
    print("I")
    print("am")
    print("function")

myFunc()
```
```
number = 0
while number < 10:
    print(number)
    number = number+1
```

## break, continue, pass
Break and continue work as in other languages.
pass is just used when we just have a comment inside the for for now, so the code compiles with just the comment. 

```
def myFunc(name):
    print(name)
    print(f"the name is {name}")

myFunc("Jay")

def myFunc(name, lastName):
    print(f"the name is {name}")
    print(f"the last name is {lastName}")

myFunc("Jay", "Smith")
myFunc( lastName="Smith", name="Jayleen")
```
Take a range from an array/list

```

array = [1,2,3,4,5]

print(array[1:3])

#print [2, 3]

```

Go all the way to the end but skip every second one

```
array = [1,2,3,4,5,6,7,8,9]

print(array[1::2])

#[2, 4, 6, 8]
```

unpacking a list
```
a,b,c = [1,2,3]

print(a)#prints 1

a,*b = [1,2,3]

print(b)#prints 2,3

a,*b, c = [1,2,3,4,5]

print(c)#prints 5


```

Set - unordered collection of unique objects

`mySet = {1,2,3,4,5}`

ternary operator

```
#return this string if this condition, else return this other string

message = "0>1" if (0>1) else "1>0"
print (message)
#prints 1>0
```

`is` is not the same as equal.  IS will compare memory locations for equality, not the values in them.  However, if we compare 1 to 1, they will be stored in the same memory because they are so simple, so `is` will return true.  This works for simple types. 2 lists with the same elementes will still have different memory locations.



## enumerate

```
for i, char in enumerate("hellooooo"):
    print(i, char)
```
prints:
```
0 h
1 e
2 l
3 l
4 o
5 o
6 o
7 o
8 o
```



Info for function in python comes between trippe quotes (''')

```
def hello():
    '''
    this is a hello function
    '''
    print("hello")

hello()
```

```
def func(*args): #accet any num of arguments with the *
    print (*args) #1 2 3 4 5
    print(args) #(1,2,3,4,5)
    return sum(args) #15
    
print(func(1,2,3,4,5))


def func(*args, **kwargs): #accet any num of arguments with the *
    print (*args) #1 2 3 4 5
    print(args) #(1,2,3,4,5)
    print(kwargs)
    return sum(args) #15
    
print(func(1,2,3,4,5, num1=5, nuym2=10))
```

If we have different types of parameters the order matters

