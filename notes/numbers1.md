We’ll move on from strings, but I’d strongly encourage everybody to practice using string methods because it will come up again and again. 
I’ll start by reposting what I said earlier about numbers since it’s buried way back there.  
What’s to say, they’re numbers. There’s integers (ints) and decimal numbers (floating point) and there’s complex numbers, but let’s not talk about that. 

There’s usually no confusion and python often handles the details for you. 
If you enter x = 5, then x is an integer
If you enter y = 3.5 then y is a float
if you enter x = 5.0 or even x = 5. thats a float

where it can get messed up is that python will do some conversion for you if necessary- see the picture below. 
if x = 5 and you enter
x = x/2, x is now of course 2.5 and has been converted from an int to a float.
if later in the code, you try to use x as an integer, you may get a “typeError” and failure. 

also note that a numerical string is not a number. 
so a= ’42’ is a string with two characters- ‘4’ and ‘2’
while b = 42 is the number 42. 

a + a will give you ‘4242’
b + b will give you 84
a + b will give you a type error. 

You can change from one type to another when you need to using python built in type conversion functions

int(a) now gives you 42
str(b) gives you ’42’
int(a) + b gives you 84

you can also convert from int to float and back

if a = 2.5
int(a) = 2

now, maybe a bit unexpected, but when you converted a to an int- python didn't forget what a used to be.  If you now enter
float(a),  a= 2.5 again. 

As you expect, you use the usual operators +, -, * and / for basic arithmetic (note you cant use ‘x’ for multiply)

In addition there is another basic operator you should get to know and love, the modulo operator %
a % b returns the remainder of a/b
so 10 % 4 = 2

This might look weird, but its super useful in certain kinds of logic like clock arithmetic. I’m gonna talk A LOT about modulo arithmetic…stay tuned.
