template literals
- When you write something inside ${} in a template literal, its result will be computed, converted to a string, and included at that position. The example produces “half of 100 is 50”
## Strings
- The way strings are ordered is roughly alphabetic but not really what you’d expect to see in a dictionary: uppercase letters are always “less” than lowercase ones, so "Z" < "a", and nonalphabetic characters (!, -, and so on) are also included in the ordering. When comparing strings, JavaScript goes over the characters from left to right, comparing the Unicode codes one by one.
	- Other similar operators are >= (greater than or equal to), <= (less than or equal to), == (equal to), and != (not equal to).
- There is only one value in JavaScript that is not equal to itself, and that is NaN (“not a number”).
```
console.log(NaN == NaN) 
// → false
```
- In practice, you can usually get by with knowing that of the operators we have seen so far, || has the lowest precedence, then comes &&, then the comparison operators (>, , and so on), and then the rest
## Empty values
- There are two special values, written null and undefined, that are used to denote the absence of a meaningful value. They are themselves values, but they carry no information. 
- Many operations in the language that don’t produce a meaningful value (you’ll see some later) yield undefined simply because they have to yield some value. 
- The difference in meaning between undefined and null is an accident of JavaScript’s design, and it doesn’t matter most of the time. In cases where you actually have to concern yourself with these values, I recommend treating them as mostly interchangeable.
## short-circuiting of logical operators
```
console.log(null || "user") 
// → user 
console.log("Agnes" || "user") 
// → Agnes
```
- If you have a value that might be empty, you can put || after it with a replacement value. If the initial value can be converted to false, you’ll get the replacement instead. The rules for converting strings and numbers to Boolean values state that 0, NaN, and the empty string ("") count as false, while all the other values count as true. So 0 || -1 produces -1, and "" || "!?" yields "!?". 
- The && operator works similarly but the other way around. When the value to its left is something that converts to false, it returns that value, and otherwise it returns the value on its right.
