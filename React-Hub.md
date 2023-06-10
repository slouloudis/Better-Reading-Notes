Master post for all react related documents. 

Documentation - https://react.dev/learn
If you want some more indepth information, it's towards the bottom of the page. I recommend reading this if you're comfortable with the DOM, browser engines, and some more details about how javascript works. 

## What is React?

React is a front-end framework for building out user interfaces. The idea behind it is that you can create your own custom components - for example, a thumbnail component, a video component, & a like button component - we can then combine these components to easily create bigger components, pages and apps. 

[What is the difference between modules, libraries, packages, and frameworks?](Modules-Libraries-Packages-&-Frameworks)

## JSX (Javascript XML)

https://hbr.org/2000/07/explaining-xml

JSX is a markup syntax - it allows us to combine HTML with our react components. Once compiled down to javascript (our browsers can't read jsx), it looks like this - 

```
import { createElement } from 'react';  

function Greeting({ name }) {  
	return createElement(  
	'h1',  
	{ className: 'greeting' },  
	'Hello ',  
	createElement('i', null, name),  
	'. Welcome!'  
	);  
}
```

And this is what it looks like in JSX

```
function Greeting({ name }) {  
	return (  
	<h1 className="greeting">  
		Hello <i>{name}</i>. Welcome!  
	</h1>  
	);  
}
```

If you're curious about the `null` part on the compiled version, that's where `createElement` would take an argument for props. 



## How to think 'in' React

Some of the info here is rephrased from https://react.dev/learn/thinking-in-react.

React is a bit of a shock to the system - prior to this, we've been happily chugging along building our apps with our classic `index.html` , `styles.css` and `app.js` files - and now we're chucking that all away. 


I highly recommend reading the react docs! 

Here are some steps to think about in the planning stage of your project. 

1. After planning out your UI, break it up into a component hierarchy. 
	 `⚡️  Something to keep in mind is the single responsibility principle - each component should ideally have a single job. Create sub components if something is getting too big. Keep it DRY! ☀️`
2. Build a version of your app that is static. We can pass data using props (much more on those later)
3. Find the minimal representation of your States
	`💫 We use state to make our UI interactive. It can be tricky at the start to identify what is 'stateful' and what is not. (See the state page for details)`
4.  Identify which components are responsible for changing 'this' state
5. Add inverse data flow **up** the hierarchy. 

If you're brand new to react, that list may not have been very clear. Don't worry! 

## Links to topics -> 


HTML and the DOM - 
When we're generating HTML, we don't really care to much about *how* our buttons or nav bars are getting themselves onto the page. What we really want is to define, say a button, and have that look the same everywhere. 

With that in mind, the most performance impactful thing we can do on our browser is write to the dom. *Manipulating the DOM is expensive*. We could create 10,000 objects instantly in JS and that would still be faster than manipulating and updating styles - remember that the browser has to repaint, do animations & load network requests all at the same time on a single threaded language. 

[[If Javascript Is Single Threaded, How Is It Asynchronous?]]

Think of a webpage like a document - like a word doc. We can edit word documents using, well, Microsoft Word. In the browser we edit our HTML document with an API. That API is the DOM. 

We've all done something like this before: 

```
const coolButton = document.getElementById("cool-button") {
	coolButton.innerHTML = "Click me! "
}
```

If the goal of react on the web is to generate HTML, how can we go about doing this in a performant way, that's easy to use and interact with. 

Lets look at a simple component: 

```
const MyComponent = () => {
	return (
	<main>
		<h1 id="title"> Look ma! </h1>
	</main>
	)
}
```

This is the object that is being spat out by react from the render function- 

```
{
	type: "main",
	key: null,
	ref: null,
	"$$typeof": Symbol(react.element),
	props: {
		children: {
			type: "h1",
			key: null,
			ref: null,
			props: {
				id: "title",
				children: "Look ma!"
			}
		}}
}
```

It's really cheap to generate these objects -  it's much faster to change these objects (as they get modified by state), as opposed to writing to the DOM every single time a change happens. This object, and it's children, are what is known as the 'Virtual DOM'







