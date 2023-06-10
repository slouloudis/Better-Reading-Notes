## Numbers 

Unlike some other programming languages, Javascript doesn't specify intergers (23) vs floating point numbers  (also called floating point literals) (2.3). The location of the decimal point will be stored in some bits.

Note that calculations with fractional numbers are not exactly precise. It is rare this will cause an issue for you. Here's a hard to understand [wikipedia article](https://en.wikipedia.org/wiki/Floating-point_arithmetic)
Here's a cool package to fix it if you do need to fix it (likely in finance) [GitHub](https://github.com/royNiladri/js-big-decimal)
If you just want to get rid of a bunch of zeros (0.2000000006) to (0.21) you can use the `.toFixed()` method. 

Just like in normal maths, we can use operators on our numbers to do calculations. BIDMAS makes a return from your maths classes too. When in doubt, add parentheses. 

The `%` operator is very useful, giving the remainder of division. eg - `215 % 100` returns `15`. 

	The % is often called the modulo. 

## Strings 

single quotes, double quotes and backticks are all fine to mark a string data type. 

If you want to enter a newline (like when you press enter) you'll need to use backticks. 

`This is one line\nAnd this a second line`

Strings, like numbers, are also modeled to bits. Javascript works off the Unicode standard. There will be some more detail about this later. 

While we can't use (most of) our normal operators on them, we can use the '+' operator, to *concatenate* the string. 

```
let x = `concate`
ley y = `nate`
console.log(x+y)

would return 'concatenate'
```

For string and numbers there are a bunch of *methods* you'll want to use. [String and Number Methods]()

**Template literals** are very useful - writing something inside the ${} means it will be computed. Use the  back tick character for these, and wrap expressions in curly braces with a $ at the start. 

```
`half of 50 is ${50 / 2}`
```

**typeof** is also a nice operator to be aware of. Using it will tell you the data type of whatever you operate on. 

```
console.log(typeof 10);
// -> number
console.log(typeof "two");
// -> string

let x = true;
console.log(typeof x);
// -> boolean
```

Some terminology. 

Operators that take two values are ***binary operators***
Operators that take a single value are called ***unary operators***

**Boolean**

True and False, "yes" and "no", "on" and "off", it's very useful to have the Boolean type. 


```
console.log(5 > 10)
// -> false
```

Strings can be compared in the same way, although it's a little more complicated. Uppercase letters are considered 'less' than lowercase ones, and for anything else you'll want to consult google. 