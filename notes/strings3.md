Strings are numbers challenges:

Python provides two very convenient built in functions for converting characters into their ASCII code numbers and back

ord(‘A’)
gives you 65, which is the ASCII code number corresponding to ‘A’ and 
chr(65)
gives you ‘A’

Open up your REPL and :

1) pick a character and print its ASCII code
2) pick a number from 32-127 and print the corresponding character
3) print the ASCII code for a few consecutive letters and note the pattern
4) print the ASCII code for a few letters in both upper case and lower case versions (like ‘A’ and ‘a’). What do you notice?
5) print the ASCII code for a few single digit numbers. What happens if you enter ord(5) ? 
what do you need to do instead?
6) choose a letter from the first half of the alphabet and print the letter that comes 10 letters after it (without counting!)

So much for  ASCII, where are the emojis?
For emojis, you need to speak unicode to python, not ASCII
Since the unicode represents so many more character, the character codes are much longer, you need 8 digits, and not only that, the 8 digits are in base 16, (hexadecimal) not the usual base 10. so each place will have either a digit or a letter A-F. Dont worry about exactly how hexadecimal works just yet, for now use the codes. 

to tell python you are speaking unicode, you begin your string with \U then the 8 digits. 

so if I tell you the unicode for eye-rolling face is 0001F644,
you can print that with 
print(‘\U0001F644’)
Try it!

7) print three different emoji symbols
