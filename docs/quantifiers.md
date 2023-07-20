
#### Regex Quantifiers

Within regex the symbols '+', '*', and '?' are called quantifiers. 

'?' means optional
'*' means match zero or more
'+' means match one or more

##### Optional
In the simplest form '?' is successful when it matches or does not match. What does this mean exactly? Let's look at this example with the word eon, or if you speak the king's english its eon. To match this word in either context we need to optionally match a followed by e then o and then n, and we can do this in regex like so:

a?eon

What this regex is saying is match a but if its not there that's ok and move on to the remaining words (which are not optional).

##### Zero or More
The '*' symbol provides us with another option but in this case we can match zero or more of the character we would like. For example consider a situation where you would have to match the following strings: bc abc aabc aaabc. We could use:

a*bc

This regex is saying match a zero or more times, and then match the remaining characters. The star allows instances when a is not there and when it appears any number of times. Contrast that with a?bc which says match a once but if its not there then move on to the rest. The '?' symbol cannot match more than once in this case though.

##### One or More
The '+' quantifier matches one or more instances. Again let's recycle the previous example and use the following regex:

a+bc

In this case we would match all the strings with the exception of bc because the '+' quantifier needs at least one instance of a to match.






