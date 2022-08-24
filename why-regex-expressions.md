# Why use Regular Expressions?

A Regex statement is simple a very finite or more scoped search criteria which is done by using some funky syntax. This can be achieved in coding applications by using expression literals. The regex statement is not just limited to one programming language and is nearly universal in its application. It is often used to validate passwords, search for text with particular criteria. Explaining this expression can be complicated so lets break it down. 

As a programmer there is a high likelihood you have tried searching through code within your code editor to check how many times and where you have called a certain variable, function, or method. The feature you have used for this is a type of formatted search. A formatted search is just one of many uses of a Regex statement. Using a find tool in a text editor is a literal search. This means that  the given the search criteria that is typed into the search field will be shown the highlighted within your document. The search criteria is chosen as you type in letters or numbers. A great question is how does the search bar work to take in the typed search with the given criteria? This could be done with a regex statement.

## Summary

A great example of a regex statement in real world application is finding or searching for a zip code. The regex offers the specific search. This is the regex statement doing our search. ```^\d{5}(?:[-\s]\d{4})?$``` . This statement is acting upon each argument that we are searching with within our regex statement. This statement will take in a string of decimals that is 5 characters long and accepts white space separated in a character set along with 4 more decimal characters.  We will take a deeper dive into the above example and break it down to understand what the purpose is and how to use regex statements.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
  Anchors are an example of the binding argument within the regex statement that refers to a position. It would be logical to think that each argument would point to a specific letter, number and symbol but it instead points to a specific position within a grouping of text, character, or character class. In our example  ```^\d{5}(?:[-\s]\d{4})?$``` we specify that the first character in the text will be a decimal with this expression  ```^\d```. The```\d``` in the expression signifies to look for decimal value at the beginning of the string while the ```^```says to match the input at the beginning of the string. Both of these are essentially doing a similar pattern and offers a double check within the expression.
### Quantifiers
Now that we know what kind of argument we can pass into a regex expression to define a specific position our next component in this expression is ```^\d{5}(?:[-\s]\d{4})?$``` identifying how many characters we would like to search for. If you have ever shopped on Amazon and filtered a search for certain material the way in which we can filter this data is very similar to a regex expression. We can now filter by amount and position of each character. These quantifiers can be identified by following the anchor tag. In this expression we are limiting the decimal characters to 5 and 4 with ```{5}``` and ```{4}``` that are each following ```\d``` . This is telling the regex statement to only look for characters passed in to be a length of 5 or 4 characters. The only clear difference between these two quantifiers is that ```{4}``` is nested within a grouping. 
 ### Grouping Constructs
Regex expressions are packed full of information arguments that can be used for filtering, sorting, and validation. Using our quantifiers and anchors together allows us to specify a specific position within a string while choosing a type of character that will fill the string. Now we can add grouping with that. In this example ```^\d{5}(?:[-\s]\d{4})?$``` that specifies a zip code we are looking for a set of numbers separated by a ```-```. Think you can already point out the grouping construct? We group by using two different methods of capturing or non-capturing. Capturing is matching a sequence while non-capturing is not. In this example we are grouping with non-capturing. The non-capturing part of the expression is is ```(?:) ```. This in basic is telling the expression that it is not mandatory to have this group to complete the search. 
### Bracket Expressions 
As we dive further into regex expressions can you think of any other real would applications of the regex expressions? Following our example after we have grouped, quantified non-capturing, and specified out anchors we are now looking for a set of bracket expressions. These bracket expressions are literally how they sound and are able to be used to match a set of characters. The bracket expression being used within the example ```^\d{5}(?:[-\s]\d{4})?$ ``` is ``` [-\s]```. This bracket expression does a couple things. First the ```-``` within the expression signifies that there will be separation of the group by a dash. Next the ```\s``` tells the statement to use whitespace in any form. White space is any spaces in between the bracket grouping. ```\s``` is a type of short hand expression within the bracket expression. This shortcut does this following action in a longer bracket expression ```[\p{Z}\t\r\n\v\f]``` which is the equivalent of ```\s```. More specifically these longer expressions can used to collate sequences and give character specific equivalents. The shorthand ```\s and \d``` is an introductory example to what a character class is. The bracket notation of ```\d``` is ```[0-9]```. Replacing these longer notations with their short hand versions will accomplish the same thing. These shorter expressions aid in the readability of the regex expression.

### Character Classes
As a programmer it is often possible to create functions that complete complex commands. For example if you are wanting to find the 5 characters we can store the operation of addition in a function and call on that function later as needed. This helps eliminate the need to right the math function every time you would like to add some integers together. We can think of Character Classes in a similar way. These classes help us differentiate letters and numbers in our regex statement in shorter way. As stated above in the Bracket Expression section, using the short hand version of the bracket notation will accomplish the same thing with less typing than its bracket notation counterpart. There may be use cases that would require a bracket notation to pick out a certain set of characters however most of the time these shorthand options are most viable.  
### The OR Operator
Inserting logic within a regex expression can take the expression to a deeper place by accepting multiple criteria. The OR operator in Javascript for example is noted as ```||```. This expression is very similar to the regex way of this expression which is ```|```. This example does not use the OR operator but in practice this OR operator could be applied to this statement ```^\d{5}(?:[-\s]\d{4})?$ ``` by also allowing letters along with decimal characters. We can do this within the given group ```(?:[-\s]\d{4})```. Adding the ```|``` after the quantifier ```{4}``` will also store and search information with the next expression. For example ```(?:[-\s]\d{4} | \w{4})```. This expression will now search for any decimal that is separated by whitespace with and additionally any characters that is a word character with a quantity of 4. This operator will allow for both of these expressions to be utilized and used and will search the text for both expressions instead of limiting to one or the other.
### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
