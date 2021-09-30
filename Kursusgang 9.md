[[_Softwaresikkerhed]]

# Strings and Metacharacters

**Todays reading**: Hacking, 2nd Edition: The Art of Exploitation, Jon Erickson chapters 1-3

## Lecture notes
[[9-strings-and-metacharacters.pdf]]

### Subjects
#### Processing strings
	
> Many of the most significant security vulnerabilities of the last decade, (1997-2007) are the result of memory corruption due to mishandling textual data, or logical flaws due to the misinterpretation of the content on the textual data
	
- Memory corruption due to string mishandling
- Vulnerabilities due to in-band control data in the form of metacharacters (e.g. ```\n``` for newline or ```\null``` to end a string).
- Vulnerabilities resulting from conversions between character encodings in different languages
	By understanding the common patterns associated with these vulnerabilities, you can identify
and prevent their occurence

- **[C String handling](https://en.wikipedia.org/wiki/Uncontrolled_format_string)**
	- In C there is no native type for strings; strings are formed by constructing arrays of the char data type, with the null character (```0x00```) marking the end of a string
	- The string is then represented by the pointer to the beginning, ```buf```

- **Exploiting format string vulnerabilities**

> A *format string* exploit is another technique you can use to gain control of a privileged program. Like buffer overflow exploits, format string exploits also depend on programming mistakes that may not appear to have an obvious impact on security. Luckily for programmers, once the technique is known, it’s fairly easy to spot format string vulnerabilities and eliminate them. Although format string vulnerabilities aren’t very common anymore, the following techniques can also be used in other situations.

*Gode at kunne til eksamen:* 
-  0x353 Reading from Arbitrary Memory Addresses
-  0x354 Writing to Arbitrary Memory Addresses
-  Plus some tips and hints for making it easier

Bad functions:
- **strncpy()** does accept a maximum number of bytes to be copied into the destination, but does not guarantee null
termination
- **strncat()** size to provide is the space left in the buffer, not the size of the whole buffer
Better functions
- **strlcpy()** a variant of strcpy that truncates the result to fit in the destination buffer
- **strlcat()** a variant of strcat that truncates the result to fit in the destination buffer
Originally OpenBSD 2.4 in December, 1998
These functions always write one null to the destination buffer

#### Metacharacters
- Null 0x00, special in C, but just another char in other languages
- Space
- / used as filename delimiters, and \ in Windows
- ```.``` dot used in various ways for domain names, file types etc.
- Comma-seperated files, using ```, . ; :``` etc.
- Special characters for syntax purposes, ```* % & | ?``` etc. Searching for everything or wild card search (bør håndteres via positivliste, som siger hvilke tegn man *må* udføre; meget svært at finde alle tegn, der skla udelukkes)
- Forskellige for forskellige miljøer (Windows, Linux, Perl, PHP, bash osv.)


#### Character sets and unicode

#### Recommendations for handling strings, how does Python help, how does Django handle strings, and input validation

#### Truncate and Encoding Attacks JuiceShop

#### Django String Handling



### Keywords
- ROP - [Return-oriented Programming](https://en.wikipedia.org/wiki/Return-oriented_programming)



#KEA/Softwaresikkerhed 