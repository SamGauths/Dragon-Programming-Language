

## Documentation
###### June 2020  
###### Written by Samuel Gauthier

### 0. Installation

First go the the official Dragon website and download the last version of Dragon in the download section. At the moment of writing these lines (June 2020) the last version of Dragon is the version 1.9.7.  
https://dragon-lang.org/dragon-197  
  
Once you have installed Dragon you will need to follow these steps to set it up (Windows):  
   __1.__ Go to control panel  
   __2.__ Click on system  
   __3.__ Click advanced system settings  
   __4.__ Click environment variables  
   __5.__ Under "System Variables" scroll to PATH  (or Path)
   __6.__ Choose PATH and click on edit  
   __7.__ Add the directory of Dragon (C:\Program Files (x86)\Dragon\Dragon Language) by default  
   __8.__ If the path does not end by a semicolon add a semicolon and hit ok.  
   
Once you have done all these steps you are ready to code in Dragon. You can code with ZDragon, the IDE that comes with Dragon when you install it or your can use any text editor of your choice.

If you need more ressources to get started you can refer to the official documentation here:  
https://dragon-lang.org/Dragon.pdf  

### 1. Comments
In Dragon, comments are ignored during the execution of the program. They do nothing, they are only used make the code easier to understand.
```
// One line comment

/* This is a 
   multiline
   comment */
```


### 2. Variables
Here are the main types of variables in Dragon: **integers, floats (decimal numbers), strings (text) and boolean (true or false)**.
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

Conditions in Dragon are pretty straightfoward. Here are some examples:
```
age = true

if(age)
{
    showln "That is true!"
} 
else
{
    showln "That is false!"
}
// Output: "That is true!"
```

```
age = 101

if(age > 21 && age < 100)
{
    showln "You are an adult"
} 
else if(age == 21)
{
    showln "You are a young adult"
}
else if(age <= 21 && age > 0)
{
    showln "You are a kid"
}
else
{
    showln "I think you are lying"
}
// In this case the output will be: "I think you are lying"
```

You can also use conditions to compare character strings. Here is an example:
```
name = "John Do"

if(name == "John Doe")
{
    showln name
}
else
{
    showln "What is your name?"
}
// Output: "What is your name?"
```
This small program with not output the text of our variable _name_ because it contains the text "John Do" and not "John Doe".
Here is a list of the **relational operators** you can use to compare values in Dragon:

&gt; greater than  
&lt; less than  
&gt;= greater than or equal  
&lt;= less than or equal  
== equal to  
!= not equal  

The other operators you need to know about are the **logical operators**. In Dragon there are three main logical operators. Those are AND, OR and NOT:

&& AND  
|| OR  
!  NOT  

This is how we use logical operators:
```
name = "Kevin"
age = 25

if(name != "Kevin" && age >= 21)
{
    showln "You can enter the bar."
}
else
{
    showln "Sorry, kids and people named Kevin are not allowed to enter the bar."
}
// Output: "Sorry, kids and people named Kevin are not allowed to enter the bar."
```
In this example, Kevin can't enter the bar even if he is old because his name is Kevin.
We can read the condition as: "if your name is not Kevin and you are 21 years old or older you can enter the bar.".  

### 5. Loops
Loops are use to repeat a part of code many times. In Dragon there are four different types of loop: **The while loop, the do..while loop, the for loop and the foreach loop**. They basically all do the same thing but some are more appropiate in certain situations.

##### while Loop
```
i = 0

while(i < 10)  // parentheses not necessary
{
    showln "Hello World!"
    i += 1
}
// Prints 10 times "Hello World!"
```

##### do...while loop
Note that the do...while loop runs the loop at least one time no matter what (even if the conditions is false). Here is the same example using a do...while loop. 
```
i = 0

do
{
    showln "Hello World!"
    i += 1
}while(i < 10)
```
Now lets see what happens if we set the value of *i* to 10.
```
i = 10

do
{
    showln "Hello World!"
    i += 1
}while(i < 10)
```
As you can see the value of *i* is clearly not less than 10 but it prints *"Hello World!"* one time. Why? Because like I said the do...while loop runs the code first and then checks the condition so it runs the code at least one time even if the condition is false.

##### for loop
Another type of loop is the __for loop__. The __for loop__ works like the __while loop__ (it checks the condition first) but it is more adapted to this kind of situation.
```
i = 0

for(i = 0, i < 10, i = i + 1)
{
    showln "Hello World!"
}
```

Here is how a __for loop__ work:
```
for(init variable, condition, incrementation)
{
    // Instructions
}
```
