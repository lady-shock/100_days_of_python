So yesterday, I didn't give you quite everything you need. We talked of loops- wile and for loops. I mentioned the idiom of the infinite loop which keeps running until the user ends it, but we didn't talk about how to get out of a loop! So ways to get out of a loop-
*break* this gets the job done quite well. as soon as you get to this statement, you leave the loop you’re in and resume program flow after the loop block ends. Make sure you know which loop you’re really in! With “nested loops, this can get tricky

*continue* this doesnt really get you out of the loop, but its so closely related to *break* that you never talk about one without the other. *continue* “short circuits”” the rest of the loops code block and brings you immediately back to the beginning of the loop code block.
*create a variable to exit the loop*
some examples of each-

```
while True:
	print(“still inside the loop”)
	break
print(“outside the loop”)```

prints-
still inside the loop
outside the loop

```
n = 0
while True:
	n += 1
	if n >20:
		break
	if n%2 == 0:
		continue
	print(n)```

prints the odd numbers less than 20 then exit the loop

```
keepLooping = True
n = 0
while keepLooping == True:
	n += 1
	print(n)
	if n == 10:
		keepLooping = False
```

prints the number 1 through 10

So far, we’ve covered:
strings
numbers
conditionals
loops
random()
range()
print()
 this is enough to land a man on the Moon! You can do all sorts of things with just this much Python. 
Next we’re going to cover lists and at that point, the rest is all just extension of those key basic ideas. 
After we do list, we need to pause and consolidate. For a while. Write lots of code. learn basic approaches to common problems. You can understand range and loops, but if youve never solved a problem using them, you wont really get it. 

Whether we restart from lists and keep going, we’ll see, it largely depends on how much engagement we have. 
prints the numbers 1
