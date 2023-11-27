So, lists…
Lists are the second Python data structure we’ll learn, (strings were the first)

A list is an *ordered* sequence of python objects. 

That’s it. 
OK, but what does that mean? Well, so far, the objects we’ve worked with are-

strings
numbers
and now lists

so a list is an ordered sequence of any of these objects. The list elements dont have to be all the same kind of objects, you can have numbers, strings and lists all as part of the same list. As we cover new object types, we’ll add to what can be in a list, but for now, this is it. 

“OK, but hold on Shock! How can a list contain a list? That makes no sense!”

Well, actually, it just works. Remember that strings are “list like”, but you probably don’t have any problem imagining a list of strings like “apple”, “banana”, “cherry”.
Having list elements in a list works pretty much the same way, you can have a list with list1, list2, list3 as its elements, and remember you can mix data types so 
“apple”, 5, list 1 works just fine too. 

We’ll leave lists with lists alone for now, but know that they are there and quite useful too. 

So list syntax and how do you make a list?
Python uses the ‘[‘ and ‘]’ to enclose a list. Putting things inside these square brackets signals that you are using a list. 

You can create a variable and assign a list to it as you create it like this

```my_list = [“apple”, “banana”, “cherry”]```

Note that each element of the list is separated by a comma
Note that each string element is enclosed in quotes, remembering that ```“apple”``` is a string while ```apple``` is a variable that could have any value whatsoever assigned to it. 

you can have lists of variables-
```
age = 21
name = “Shock”
favorite_food = “pizza”
my_data = [age, name, favorite_food]```

works just fine. 

Just like you can crate an empty string with ```my_string = ‘’```
You can create an empty list with ```my_list = []```

Why would you want to do this? Most often, you might have a list that you want to add to every time you make a pass through a loop. You cant define the list inside the loop, because if you do, every time you go through the loop, the list gets changed back to that definition, it wont get any longer at all.
Before the loop starts, you don’t have anything to put into the list yet, so the solution is to create an empty list outside the loop and add to it with each pass through the loop.
We’ll see examples of this later.

Another way to create a list is to use the list() function. This is pretty clever. It takes an object with elements you can count (remember we called that an ‘iterable’ when we talked about for loops) and turns it into a list. 

So far, the only iterables we’ve covered are strings and range() objects. And they both work. 

```
my_string = “Shock”
my_list = list(my_string)
print(my_list)```

prints [’S’, ‘h’, ‘o’, ‘c’, ‘k’]

and 
```
my_range = range(5)
my_list = list(my_range)
print(my_list)
```
prints 
[0,1,2,3,4]

note that numbers inside a list *don’t* get enclosed by quotation marks. 
Remember the difference between 5 and ‘5’. 
The first is a number, the latter is a string. 

OK, last point, I left you hanging on that definition of list- 
an ordered sequence of objects. 

what do i mean by “ordered”?
Well, as you’d expect, when you create and manipulate a list, Python keeps track of the order of each element. That order doesnt change unless you make changes to the list. (This is not necessarily true of later data types we’ll be covering)

Like strings, you can refer to a specific element of a list by referring to its *index* position. 
By convention, the first element of a list is given the index of 0 (hence a zero-indexed data type). You will hate this at first, because who starts counting at 0? You even have to make up a new word to refer to it as the ‘0th’ element of the list because the first comes second!
That’s horrible, I know. Why does Python inflict that on us? For now, let’s just say that it will eventually make a lot of the operations you do like looping through one item of a list at a time much more logical. You may never learn to like it, but you’ll get used to it. Promise. 

To refer to an element using it’s index, you use the same [ ] notation.  So 

```
my_string = [“apple”, “banana”, “cherry”]
print(my_string[0])
```

prints
apple

There’s tons more to go over about lists and how you can manipulate them. You must get *very* comfortable with this. So we’ll stop here and pick up again tomorrow…
