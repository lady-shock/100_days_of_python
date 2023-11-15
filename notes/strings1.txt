So lets slow down and even go back a bit. One week ago, we learned about strings. @⁨Abraham⁩ is absolutely right, we could spend 4 days on strings and still have more to learn. Let’s make sure everybody here is good with strings and some  basic things you can do with them. If youre not, ask!

From whatever resource you are using, read or watch what they have to say about strings. A few comment from last week:

Let’s talk strings…strings are a python basic data type, a sequence of 0 or more characters. We’ll be getting to python lists soon- they are similar to lists, but with some important differences.
You’ll read the term ‘string literal’- that just means a string enclosed in quotes, as opposed to a string variable (to which a string literal has been assigned). 

“aString” is a string literal, which is simply to say it is a string. 
if you say 
myString = “aString” , myString is a string variable whose value is the string “aString”

You can create an empty string variable with
emptyString = “”
and add to it as you need. 


Things you do with strings:

1) pass (give) them to functions (i know, we havent got to functions yet) like 

print(aString) or 
print(“aString”) .  

Know the difference between those two statements. Later we’ll do a lot of passing strings to functions. 

Another often used function is len(), which when given a string, returns the number of characters it has. So-

myString = “Hello”
myStringLength = len(myString)
print(myStringLength)

prints 5.

note you could also just have written-
print(len(“Hello”)


2) use python operators on them. An operator is a symbol with a defined meaning. When we deal with numbers, symbols like +, - or * have the same meaning as in arithmetic. For some operators, python defines a meaning to make it work with strings the way you might expect. 

So you can use + to join two strings together. "first” + “name” becomes “firstname”. Note that python won’t put a space between the strings, if you want “first name” you must enter “first “ + “name”. Note that both operands MUST be strings, python will not convert other data types for you if you mix them. 

print(“hello “ + “world”)

prints ‘Hello world’ just fine but 

print(“hello” + 4)

causes a typeError

Similarly, you can use the * operator. Less commonly used, but for example 
print(“string” * 3 )

prints “stringstringstring”

3) string methods-python has many builtin methods to manipulate strings. A method is pretty much a function but the syntax is subtly different. You “pass” a string to a function like print(string). But you apply a method to a string with “dot” syntax like 

string.upper() So-
myString = “hello”
myStringInCaps = myString.upper()
print(myStringInCaps)

prints ‘HELLO’


String methods are incredibly useful (and fun!). You’ll use them all the time.  Here’s a website I think you all should bookmark and visit often- this page is a very handy list of string methods

https://www.w3schools.com/python/python_strings_methods.asp
