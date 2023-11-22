So lets talk loops and range():
We’ll do this and lists then take a pause to really consolidate. Because there’s a *ton* of great stuff you can do with just this much. IMO, learning how to use these basic tools is absolutely vital no matter where you ultimately go- machine learning, data science, automation, game design, whatever…

Python gives you 2 loop styles to use, *for* loops and *while* loops. You can use whichever you like and often it just a matter of which feels more natural to do what you are wanting to do. Any *for* loop can be written as a *while* loop and vice versa. 
In general, I’d say that if you want to “do something” a certain number of times (even if you don’t know how many until the code runs), a *for* loop works best. If you want to “do something” until a certain condition is met, then you probably want a *while*  loop. 

*for*:
a for loop is written like this-
```
for variable in iterable:
	do something
	do something else
```
Here ‘variable’ is just a name you choose (more on this later) and ‘iterable’ is the name of something you can ‘ iterate’ over. 
“Wait Shock, foul! You haven't said what iterate over means!”
Right. ‘Iterable’ refers to any python object that you can count the elements of. So far, the only iterable we know is a string. You can count the elements of a string, that’s what len(string) does. So “hello” has five elements. 
That’s it. Thats the only iterable we’ve looked at. 

So a for loop like this-
```for variable in “hello”:
	do something```
the loop will “do something “ 5 times, once for every character in “hello” 
(note that if you already had a variable like say=“hello”, then the loop could begin as ```for variable in say:```

if ‘do something’ makes use of the character (like printing it), then you must use the same name as you began the loop with. As in-
```for variable in “hello”:
	print(variable)```

Now, that’s a bit awkward, right? So by convention, you give ‘variable’ a better name, here ‘letter’ would be a nice choice-
```for letter in “hello”:
	print(letter)```
Same code but better, right?

Both code snippets would  output- 
‘h’
‘e’
‘l’
‘l’
‘o’

And like indentation in if blocks, you indent each of the lines within the loop the same amount and then stop indenting when the loop code is done.

OK, iterating over a string is good, but it would be nice to have other objects to iterate over. Soon enough we’ll have many more but for now, lets just add one- a ‘range’.
 
Pythons ```range()``` function creates a list-like (remember, strings being ‘list-like’?) which is just a sequence of integers.  The syntax is identical to the ```randrange()``` function from the random module- you tell python where to begin, where to end and how many to increase by in each iteration.  In exactly that order

If you give one value -
```range(n)``` starts at zero and increases by 1 up to n (but not including n)
```range(3)``` consists of 0,1, and 2

If you give 2 values-
```range(m,n)``` starts at m and increments by 1 up to but not including  n
```range(10, 15)``` consists of 10, 11, 12, 13, 14

If you give 3 values-
```range(m, n, i)``` starts at m and increments by i up to but not including n
```range(1, 11, 2)``` consists of 1, 3, 5, 7, 9

Its not as complicated as it sounds. So lets try it:
As always, naming variables well is useful in keeping your code readable. When iterating through a sequence of integers, ’n’ or ‘number’ are good choices

So-
```for number in range(4):
	print(number)```
the output is 
0
1
2
3

```for number in range(1, 4):
	print(number)```
outputs-
1
2
3

```for number in range(1, 4, 2):
	print(number)```
outputs-
1
3

Of course, you can do more interesting things with each element as you iterate through the range

```for number in range(4):
	print(number * number)
```
outputs-
0
1
4
9

OK, enough for one day. For loops and range(). Think on that and I’ll add a few exercises. Next while loops. Then list. Then we will work a lot with what we have.
