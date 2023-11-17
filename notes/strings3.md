So let's keep talking strings. this is long, sorry. 
 
Yesterday, I said that a string is a list-like sequence of characters, but I didn't say anything about what a 'character' is. In some programming languages, (like C) a character is a basic data type and you work directly with them - they dont really have 'strings', just lists of characters. There's no built-in string methods (although being so useful, people create and share them). Python handles a lot of that detail for you but in the end, python is built on C, so deep under the hood, it's still using characters. Python has no character type, a character is just another name for a string of length = 1
Now, your computer doesn't know or care about characters. The idea of 'A' has no meaning to it. Internally, if you need to assign the letter 'A' to a variable, python instead places a number corresponding to the letter 'A' into memory (which happens to be 65, or in 8 bit binary 00100001). If you have a string variable = 'ABC', python stores a sequence 

001000010010001000100011

Each block of 8 digits corresponds to one letter. 
If you ask python to manipulate the string, it just moves those digits around without thinking about letters.
If you ask python to print an 'A', somewhere there is a table which python uses that tells it for the number 00100001, send a pattern of pixels to the screen that looks to us like the letter 'A'

Where do these numbers come from? The basic character codes comes form a table called ASCII. 
https://en.wikipedia.org/wiki/ASCII
Each character gets its own ASCII number from 0-127.  ASCII goes way back to telegraph machines and evolved through typewriters and teletype terminals. So it doesn't start with 'A' = 0, like you might do if you were inventing your own table today. Instead, the first 32 character are mostly weird obsolete nonprinting codes like 'bell' and 'line feed'. Actual printing characters begin at 32 with punctuation and numbers and the letters don't start until 'A' at 65 and go through 127. 

ASCII itself is obsolete because it is limited to the character sets of just a few languages, never mind emojis. 
So the original ASCII has been extended into 'unicode' which covers nearly all languages (and emojis!)

OK, so why is all this important, who cares what is happening deep down in your computer?

Well, it can be very useful at times to work with characters as numbers, when sorting, for example. Or when transforming one letter into another like converting upper case to lower case, counting the distance between letters. And most importantly, how else is your code going to print emojis?

Open your REPL and try it out. 
You already know that you can use some operators with strings - you can enter 

’apple' + 'banana’

and the REPL replies 'applebanana'
You can't subtract, 

'apple' - 'banana'

But you CAN use < and >

'apple' < 'banana'

replies True, which makes sense

'apple' < 'Banana'

though, replies False. Why? If you don't understand, sorting will fail. 
Likewise-

'1' < '5'

is True, like you expect, but 

'5' < '4242'

is False. Why? Again, all sorts of sorting bugs come from this- 
imagine you are collecting user input of test scores and they enter '3', '5', '12' , '19' and '20'- you want to print the highest and lowest- what to do?

And lastly, of course, the most important reason- printing emojis!!
