
#JavaScript Data Types and String Methods

After the lesson, you'll be able to understand:
+ JS data types
+ Strings and string methods
  + length
  + upper and lower case
  + concatenation
  + charAt
+ String indexing

## Data Types
When we want to do something meaningful with a computer, we have to tell the computer how we want it to treat our data - is that set of 1s and 0s supposed to be words? Or numbers? Or something else? Depending on the type of data we tell the computer to treat it as, we can instruct the computer to do different things with it.

JavaScript has a just a few different data types. We’ve played with two of them already - numbers and strings. Javascript recognizes numbers and strings when we write them - numbers it interprets as decimal numbers, and anything between double(" ") or single(' ') quotes is treated like a string. The rest will become more useful to us later on as we continue to code.

1. **Number**: 1, 3.14, 0.13, -100, …  
2. **String** (as in, a string of characters). examples include: "a", 'World Wide Web'
3. **Boolean**: Represents true or false
4. **Undefined**: has not been assigned a value, so the value is unknown
5. **Null**: This is a special keyword that means one of two things: no value or empty. The difference from undefined is that when a variable is null, it is still defined

## String Methods and Properties
We've already seen what numbers can do - math operations, like addition, subtraction, and multiplication. Let’s play with our string data type. Let’s take one of our college variables that has a string for a value:
```
>var collegeText = "Intro to CS"
```
A method is a function attached to a piece of data. Often, it is a set of actions that can be performed on the data. When a method is called on a string, it modifies that string based on that set of actions. JavaScript has a number of built in methods that we can call on strings. The syntax for calling methods is dot notation, which looks like this:
```
variable.method()
```

### Some String Methods

Many times, you can open up the JavaScript console to test what a certain method does. The following examples use a variable, my_text:

> `my_text = "cssiRocks"`

**.charAt(x)** - Returns the character at the “x” position within the string
```
> my_text.charAt(0) 
< "c"
```
**.concat(string1, string2)** - Combines one or more strings (arguments) into the existing one.
```
> my_text.concat("duh")
< "cssiRocksduh"
```
**indexOf(substr, [start])** - Searches and (if found) returns the index number of the searched character or substring. If not found, -1 is returned.
```
> my_text.indexOf("r")
< -1
> my_text.indexOf("R")
< 4
```

**substr(start, [length])** - Returns the characters in a string beginning at “start” and through the specified number of characters, “length”. If length is not included, this function returns the remaining characters.
```
> my_text.substr(1,4)
< "ssiR"
```

###Different Method Syntaxes
Sometimes, there are multiple syntaxes that do the same thing.
```
> "one ".concat("two")
"one two"
>"one " + "two"
"one two"
```
When we add strings to each other, we stick one right on the end of the other. This is called concatenation, and we can do it with the .concat() method, or with the '+'.



### Assigning Variables and Stringing Methods
You can make a new variable from the result of a function call.
```
> var bigColor = "pink".toUpperCase()
```
You can chain functions - call a function on the result of another function:
```
>"yellow".substring(0,4).toUpperCase()
```
You can combine these tricks. You can even store the resultant value in the same variable you started with!
```
> var lemonColor = "yellow"
> lemonColor
> lemonColor = lemonColor.toUpperCase()
> lemonColor
```
The key to understanding this mind trip is that JavaScript handles everything on the right side of the "=" before dealing with the left side.

We can also call a property on string to find out some valuable information about it, using the length property.
```
var lemonColor = "yellow"
> lemonColor.length
```
You can see since length is a property rather than a method, its notation does not include parenthesis () at the end.

**Challenge:**
Given the string  var text = "ELEPHANTBEARMOUSECOW" , make the 'MOUSE' portion into a lowercase 'mouse'.  Store the value back into 'text'.

Not sure how? Remember you can also search the web for documentation on js
string methods, talk to a classmate, or consult your ducky droid!

##Resources
[W3 Schools String Methods](http://www.w3schools.com/js/js_string_methods.asp)

[15 JavaScript String Functions](http://www.sitepoint.com/15-javascript-string-functions/)
