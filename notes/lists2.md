Staying on the topic of lists-
Last time, I showed how to create a list either empty or with data in it. And I said that one important thing about lists is that you can change them- add to them, remove from them, slice them, reverse them, all sorts of thing you can do. But I didn't say much about how you do that.

Adding to a list
 
one way to add to a list is to use the + operator. This will add the new element to the end of the list. Remember that you can use the += operator as a shorthand for adding something to a variable-

 
my_age += 1

is the same as 

my_age = my_age + 1

just more concise.  Either way, I just got a year older.


It works the same for lists-


my_list = [‘apple’, ‘banana’, ‘cherry’]
my_list += ‘dragon fruit’

now, my_list = [‘apple’, ‘banana’, ‘cherry’, ‘dragon fruit’]

Another way to add to a list is the list append() method. 
Remember that when you use an object’s method, the syntax is to state the object.method(argument) (which sounds more complicated than it is) . For example, 

my_list.append(‘eggplant’) 

adds ‘eggplant’ to the end of my_list, so now 
my_list=  [‘apple’, ‘banana’, ‘cherry’, ‘dragon fruit’, ‘eggplant’]

But what if you don’t want it at the end?
No problem, now you use the insert() method. 
Like append(), you call insert() on your list with the ‘.’, but here you give it 2 arguments- index (where it goes) and element (what to put there)
Remember that lists are zero-indexed meaning the numbering starts at 0. Insert()  will insert your new element so that it takes that index position and moves everything after to the next higher position (also less complicated than it sounds)
So-

my_list.insert(1, ‘fig’)

and now my_list =  [‘apple’, ‘fig’, ‘banana’, ‘cherry’, ‘dragon fruit’, ‘eggplant’]
fig although its index is 1, is the second element. ‘banana’ which was 1, is now 2

Let’s ignore the last way to add to a list which is extend(). Know that it exists, and that it adds a second list to your original list. But we’ll come back to lists that have elements which are themselves lists

Removing items from list
again, there are several ways to do this

the list pop() method is the simplest (the name ‘pop’ refers back to older programming languages where you would ‘push’ a variable onto a stack and ‘pop’ one off)
By default, pop() removes the last element of the list
So 

my_list.pop()

now my_list = [‘apple’, ‘fig’, ‘banana’, ‘cherry’, ‘dragon fruit’]

What if you want to remove an item other than the last one?
you simply give pop() the index of the element you want to remove. 
So to remove the 0th element-


my_list.pop(0)

now my_list = [‘fig’, ‘banana’, ‘cherry’, ‘dragon fruit’]

Which is how you remove an item when you know its index.

What if I want to remove “banana” without having to figure out what it’s index is?

Thats your remove() method

my_list.remove(‘fig’)

now my_list = [‘apple’, ‘banana’, ‘cherry’, ‘dragon fruit’]

Lastly, to remove all elements- my_list.clear(). I’ve never actually used this because its the same as my_list = [ ]

Thats enough for one day- but basically a few methods to add elements, and a few to remove elements.  

Next we’ll move on to slicing and iteration…
