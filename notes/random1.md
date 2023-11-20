We're still talking about numbers, today my favorite kind of numbers, random numbers!
Python provides you the tools (functions) to do some really cool things very easily with random numbers. Now we haven't talked about functions yet, even though we have been using them with the print() and len() functions. Its been pretty intuitive even though we haven't dived deep into the topic of functions yet. 
While there a quite a few functions dong different kinds of random things, we will stick to just two today, randrange() and seed(). 

Now unlike print() and len(), even though the random functions are a part of your Python installation, you cant actually use them without adding a line of code to "import" the random module. There are several variations of the import statement, for now we will just use one. Place this line at the beginning of your code either in the REPL or in a file you are editing -
```import random```
That's it. Now python has access to all of the many functions in the random module. To use one of them, you place the name of the function after 'random.' and then place parentheses after the name. So:
```random.randrange()```
runs the randrange function of the random module. A bit confusing at first, yes. To actually make it do something by putting "arguments" into the parentheses ( just like with print("hello world") or len(str)).
The randrange function requires either one, two or three arguments. All three must be integers (or something that evaluates to an integer like (4 + 5) or len(myString)) and you separate each argument with a comma. 
If you use randrange with just one argument like:

```random.randrange(10)```
randrange will give you a randomly chosen integer from 0 up to but not including, 10. In other words >= 0 and <10. So it will NEVER give you 10. If you want 10s, then it's
```random.randrange(11)`
If you give randrange two integer arguments like 
`random.randrange(1,100)```
randrange will give you an integer >=1 and < 99. In other words, you've set a floor for the lowest integer you'll get that might be  something other than 0. Note that 
```random.randrange(n) ```is the same as 
```random.randrange(0,n)``` 
Either way is fine

Lastly, if you give randrange thre integers like this:
```random.randrange(0, 100, 2)```
randrange will choose an integer >=0 and <100, but stepping by 2s. So 0, 2, 4, ...99. Note that if you are starting at 0, you MUST give 0 as the first argument, because if you only use 
```random.randrange(100, 2)```
you're actually asking for an integer >= 100 and < 2 and you wont get what you want.

If random numbers aren't your thing, feel free to stop here, others read on...
"But Shock!" You say. "Computers dont do anything randomly, how can you get a truly random number?"
Well, actually computers _can_ be random by using thermal noise or other random inputs, but here, you're right its not.  Under the hood, random takes an _almost_ random number called a "seed" and does an incredibly complicated set of arithmetic operations on it And transforms it to a "pseudorandom" number in the range you asked for. Each subsequent number it gives you uses the one before as its input. Practically speaking, its almost random because it uses the seconds part of the current time but to the nearest nanosecond and that number moves so fast that its all but random. 
So good enough for most purposes. But tuck away in your mind that its not "cryptographically" secure, because knowing the algorithm and the first random number it spits out, you can calculate what the next one will be. Good if you are playing video poker, but bad security. Nothing we'll be doing any time soon, so dont worry for now. 
So what about the "seed" function I mentioned? "
random.seed() gives you a way to specify the number that will be used for the seed so that you are guaranteed to get the same sequence of "random" numbers each time your program runs. 
"Wait a minute, that's dumb. Why would I want that?"
Well, for testing purposes, perhaps but more often to make sure everybody is using the same random data. So if I was to give you a challenge to add 1000 random numbers together, I'd have no way to know if you got the right answer or not. But if I give you the starting seed, everybody will get the same input. 
So how do you use seed()?
```random.seed(42)```
sets the starting seed to 42. That determines what the first random number will be and every number after that until you give a new seed.
That might not be immediately clear until you give the exercises a try...
