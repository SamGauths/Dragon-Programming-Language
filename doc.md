

## Documentation

### 1. Comments
In Dragon, comments are ignored during the execution of the program. They do nothing, they are only used make the code easier to understand.
```
// One line comment

/* This is a 
   multiline
   comment */
```


### 2. Variables
Here are the main types of variables in Dragon: integers, floats (decimal numbers), strings (text) and boolean (true or false).
There are other data types like arrays, maps, objects and functions.
```
a = 10  // integer
b = 2.09  // foat (deciaml number)
c = "Hello World!"  // character string
d = true  // Boolean (true or false)
```


### 3. Input/Output

In Dragon, if you want to print a text in the console you don't even need to add a library. You simply need to use the command __show__ or __showln__:
```
show "Hello World"
// This will output "Hello World!"
```
You can use also use __showln__. It will add a line-return at the end of the text.

Now lets say you want to print the value of a variable. You simply have to write the name of your variable beside the command __show__:
```
a = 420
b = 69.96
c = "Hello There!"

showln a   // 420
showln b   // 69.96
showln c   // "Hello There!"
```

If you want your program to take an input it is also very simple.
```
select "std"

x = readln()
showln x
```
This simple 3 lines program ask the user to enter something and then prints what has been entered by the user.
Ps: Don't forget to add the __std__ module. This module contains many standard functions like __readln()__.


### 4. Conditions

