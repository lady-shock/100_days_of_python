Let’s talk while loops-
As i said yesterday, a *while* loop is one of two ways Python gives you to express a loop, so that you can repeat a block of code as many times as you need without retyping it each time. Very useful.
The syntax for a *while* loop is a bit simpler-
```while(something remains true):
	do stuff```

inside the () you put some condition to test and everything in the code block (each line thats indented after the *while* line gets done until that condition is no longer true. So lets say you want to print the square of every number until the square exceeds some value-

```

number = 1
while (number **2  < 30):
	print(number ** 2)
	number += 1```

will print-
1
4
9
16
25

Note that the variables used _inside_ the loop were all declared _before_ the loop. 
Why?
Well, if they were declared _inside_ the loop, they would get reset each pass through the loop. Also, if you are using the variable name in your test condition, if you haven't declared it before, when you get to the *while* python hasnt seen it named yet, so you’ll get a nameError

```
while(n < 10):
	print(n)
	n += 1
```
Fails because there is no ’n’ declared.

and here-
```
n = 0
while (n < 5);
	j = 2
	print (n ** j)
	n += 1
	j += 1```
doesn't do what you want because even though you increment j each pass through th loop, it gets reset to 2 every time.

As I said yesterday, a while loop can always be writen as a for loop, if you adjust the syntax. 

so 
```
n = 1
while (n < 5):
	print(n)
	n += 1
``` 
does the same as 
```
for n in range(5):
	print(n)
```

Its your choice, both are equally correct

Last point- it is a common thing to want a loop to loop forever until the user stops it. 
So a standard way to do this is to use a test condition that is always true. 

```
while( 2+2 == 4):

while True:

while 1:```

are all ways to create such an infinite loop. Just remember to provide the user a way to stop it or they’ll have to crash terminate your program!
