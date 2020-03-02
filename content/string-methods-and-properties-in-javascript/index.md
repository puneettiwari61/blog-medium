---
title: "String Methods and Properties in JavaScript"
description: "Today I am going to write about all the important string methods and properties with examples. I won’t be writing about deprecated methods."
date: "2019-11-23T12:02:59.337Z"
categories: []
published: true
canonical_link: https://medium.com/@puneettiwari61/string-methods-and-properties-in-javascript-395afe34733d
redirect_from:
  - /string-methods-and-properties-in-javascript-395afe34733d
---

#### Let’s play with Strings without wasting a moment.

```
let str = 'Hello World'; //I m going to use this string as an example to explain all methods.
```

1.  **Length Property**

```
str.length ; //it returns the length of string
11
```

2\. **charAt( ) ;**

```
str.charAt(3);
"l"
//it takes index as parameter and returns the character at that index.
```

3\. **charCodeAt( ) ;**

```
str.charCodeAt(3) ;
108
//takes index as parameter and returns an integer between 0 and 65535 representing the UTF-16 code
```

4\. **concat( );**

```
let str2 = “ this is js” ;
str.concat(str2);
“Hello World this is js”
//it takes other string as a parameter and returns a new string after combining them.
//does it mutate => No
```

5\. **endsWith( );**

```
str.endsWith('d');
true
str.endsWith('e');
false

//it takes two parameters one is character or characters and another is the length of string(upto the length you want to check), if second one isn't provided it takes length as default length of string.
//it returns true or false, if first parameter exists at the end of string it returns true or else false.
```

6\. **includes( );**

```
str.includes('d');
true
str.includes('e',2);
false

//it takes two parameters one is character or characters and another is the index you want to start your search with , if second one isn't provided it takes 0 as default index.
//it returns true or false, if first parameter exists in the string it returns true or else false.
```

7\. **indexOf( );**

```
str.indexOf('e');
1
str.indexOf('o',5);
7
str.indexOf('k');
-1

//it takes two parameters one is character or characters and another one is optional, which is the index you want to start your search with , if second one isn't provided it takes 0 as default index.
//it returns index of first occurrence of parameter and if it dosen't exist it returns -1.
```

8\. **lastIndexOf( );**

```
str.indexOf('o');
4
str.lastIndexOf('o');
7

//it is similar to indexOf , but it returns the last occurrence of character we searched and -1 , if not found.
//as we can see in above example 'o' comes two times in string , in indexOf it returns its first occurrence but in lastIndexOf it returns the last occurrence .
```

9\. **padEnd( );**

```
str.padEnd(12,'!');
"Hello World!"
str.padEnd(15,'!');
"Hello World!!!!"

//it takes two parameters one is the length of output string and second optional parameter, the string you want to pad , if not provided it takes " " as a default parameter.

//it returns a new string of the length specified in first parameter with applied pad string at the end of current string.

//it will repeat or truncate the pad string depending upon the 
specified output length.

//if specified length is less than current string it returns the string as it is.

does it mutate => No
```

10\. **padStart( );**

```
str.padStart(14,'Yo!');
"Yo!Hello World"

str.padStart(17,'Yo!');
"Yo!Yo!Hello World"

//it takes two parameters one is the length of output string and second optional parameter, the string you want to pad , if not provided it takes " " as a default parameter.

//it returns a new string of the length specified in first parameter with applied pad string at the beginning of current string.

//it will repeat or truncate the pad string depending upon the 
specified output length.

//if specified length is less than current string it returns the string as it is.

does it mutate => No
```

11\. **repeat( );**

```
str.repeat(2)
"Hello WorldHello World"

//it will take a number as parameter.
//it returns a new string containing the specified number(parameter) of copies of the given string.
does it mutate = No
```

12\. **startsWith( );**

```
str.startsWith('He')
true
str.startsWith('He',2)
false

//it takes two parameters one is string and another is the position you want to start search with, if second one isn't provided it starts with 0.
//it returns true or false, if first parameter exists at the beginning of string it returns true or else false.
```

13\. **toUpperCase( );**

```
str.toUpperCase();
"HELLO WORLD"

//it returns a new string after converting its characters into uppercase.

does it mutate => No
```

14\. **toLowerCase( );**

```
str.toLowerCase();
"hello world"

//it returns a new string after converting its characters into lowercase.

does it mutate => No
```

15\. **trim( );**

```
let myName = "  john  ";
myName.trim();
“john”

//it returns a new string after removing whitespace from both sides of string.

does it mutate => No
```

16\. **trimRight( ); or trimEnd( );**

```
let myName = "  john  ";
myName.trimRight();
"  john"
myName.trimEnd();
"  john"

//it is similar to trim but just removes whitespace from end of string, and returns a new string.
```

17\. **trimLeft( ); or trimStart( );**

```
let myName = "  john  ";
myName.trimLeft();
"john  "
myName.trimStart();
"john  " 

//it is similar to trim but just removes whitespace from beginning of string, and returns a new string.
```

18\. **substring( );**

```
str.substring(1,7);
"ello W"

//it takes two parameters, first is the position of first character to include in the returned substring. and another is the position of first character to exclude from the returned substring.

//it returns a new substring which includes the character of first parameter but excludes the charcter of second parameter.

does it mutate => No
```

19\. **split( );**

```
str.split(' ');
(2) ["Hello", "World"]

str.split('');
(11) ["H", "e", "l", "l", "o", " ", "W", "o", "r", "l", "d"]

str.split(' ', 1);
["Hello"]

str.split('e', 2)
(2) ["H", "llo World"]

//it is one of the most used method as it returns an array from a string.

//it takes two parameters, first is a separator, it can be a character or characters which is present in current string and another which is a non-negative integer limiting the number of splits.

//both parameters are optional.

//it returns an array of strings, split at each point where the separator occurs in the given string.

//if we won't put any parameters, output will be an array of string.
str.split();
["Hello World"]
```

20\. **slice( );**

```
str.slice(1,7);
"ello W"

//it is very similar to substring method.

//it takes two parameters first is beginIndex and another is endIndex.

//it returns a new string containing the extracted section of the string, similar to substring.

does it mutate => No
```

### Lets see difference between substring( ) and  
slice( )

\=> Substring requires positive indexes and will set a negative index to 0. Slice’s negative index means the position from the end of the string.  
\=>Substring will reorder the indexes to make the first index less than or equal to the second index.

21\. **replace( );**

```
str.replace('ello','p');
"Hp World"

str.replace('el',8)
"H8lo World"

//it takes two parameters, one is the substring which we have to replace and another is a new substring which we have to replace.

//it returns new string after replaceing its first occurrence  substring by new substring.

does it mutate => No
```

**So these are all the most used strings method, supported in almost all browsers.**
