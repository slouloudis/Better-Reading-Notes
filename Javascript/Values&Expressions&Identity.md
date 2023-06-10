
All values are expressions, but not all expressions are values. 

Imagine you're in a coffee shop, and ask the person behind the till for an americano. The barista makes the drink for you (like magic!) and hands it back to you. You've *expressed* that you wanted a drink, and the barista (our browser) has handed the result (the value) back to you. On the otherhand, if you gave the barista an americano already in your hand and then asked for an americano, she'd probably look at you oddly and hand it back to you. 

`2 * 10` is an expression
`20` is a value *and*  an expression

You can confirm this by typing a value into a JS console - you'll see that it just returns the value. 

> [!NOTE] This isn't the same for all programming languages  
> In some languages, such as Lisp, expressions *are* values and can be manipulated. I would give more info, but I don't know it. 


**Values** refer to things such as numbers, strings, functions and so on. We need values to organise our data into chunks, otherwise we'd just have 30-billion bits floating about in our volatile memory which wouldn't be very useful. 

If we want a value representing 42 in our program, all we have to do is type it in. Easy! Now we'll have the bits of `101010` in memory, represented in binary. 

[CompSci 1010 - What is binary?](CompSci 101.-What-is-binary)

There are two main things to be aware of when comparing things in JS. 

Let's compare some numbers. 

```
42 === 42
// -> true
```

It is true that 42 is that same as 42. Thanks Js. 

Let's compare something a bit more complicated. We're using the strict equality operator here. 

```
(function () {}) === (function () {})
// -> false
```

We've compared two empty functions to each other, but the result is false. The same thing will happen if you compare two arrays that are the same. 

```
[1,2,3] === [1,2,3]
// -> false
```

Two keyword and concepts to remember - 

Passed by value - Primitive data types, meaning: Strings, Numbers, Null, Undefined and Boolean are compared by their value. 

Passed by reference - Objects, arrays and functions are compared by their *reference* to a location in the computers memory. When we made the arrays earlier, even though they held the same data types, they hold different references to their storage location, so they are not the same. 

