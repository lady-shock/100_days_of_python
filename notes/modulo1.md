Lets talk more about numbers! As you know, Python gives you the standard arithmetic operators: +, -, * , and /. They do pretty much what you'd think (except remember to watch out for unexpected conversion from integers to floats when dividing!) The  **** operator is for powers, 2 ** 3 is 2 to the third power or 8.

Now, we come to my favorite operator, % also known as the modulo operator. (Note that in Python, % has NOTHING to do with percentages). This underappreciated operator is at the heart of cryptography, clock arithmetic and the celestial orbits of heavenly bodies. IMO, its a crime that we dont teach it in elementary schools (at least not here)
% is quite simple. For two integers, a and b:
a % b is the remainder after a is divided by b.
So-
10 % 4 = 2
42 % 6 = 0
and so on.

"But Shock! What good is that?" Well, % is super useful for doing calculations on anything cyclical like a clock. If I tell you the bus arrives every 17 minutes starting at midnight and its now 4 am when does the next bus arrive? ( I dont really want to know yet, just showing and example)
Some things that might not seem cyclical in fact are. I know everybody is dying to code "rock, paper, scissors". And everybody codes it the same way- with a bunch of if statements like "if computer chooses rock and player choses paper then player wins".  And you _can_ do that. And I _will_ ask you to.
But 

a) it's boring and repetitive
b) there's a better way using %
c) Shock being Shock is going to ask you to code an advanced variation of rock, paper scissors  that would require 20 separate if statements. And you _dont_ want to write 20 if statements.

Think about it for a moment? Do you see how the rules of rock, paper, scissors follow a cyclical logic? Can you picture a clockface with only three markings, 'R', 'P' and 'S'? How can you look at it and tell which choice wins or loses?

And OK, as much fun as rock, paper, scissors is what's even better is that % is one of the keys of modern (and ancient) cryptography. One reason is that % can make a function _irreversible_. Meaning lets say a have a simple algorithm that is publicly known to encrypt my secret number so you dont know what it is. Let's say that algorithm is I take my secret number and square it (cipher = plain ** 2). So if my secret number is 7, in my code, that becomes 49. Well, thats not keeping it secret, is it? Since you know my algorithm, if you see 49, you know my secret number was 7 by taking the square root of 49. So thats a _reversible_ algorithm and no good. 

Now lets say my algorithm is to take the %10 of my secret number. (cipher = plain % 10). Even if you know my algorithm, if my secret number is 42, this encrypts to 2. Now, if you see 2, you have almost no idea at all what my secret number is. it could be 2, or 12, 22, or 3454968574345432.
So % is an _irreversible_ operation. This turns out to be __very__ useful…
