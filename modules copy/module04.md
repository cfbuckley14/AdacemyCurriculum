# Module 4 - JavaScript Basics

## Objectives

- Understand what JavaScript is, its origins and how it works
- Understand the structure of JavaScript and clearly explain the data types
- Ability to build and manipulate data using JavaScript
- Ability to interact with the DOM using JavaScript
- Understand JavaScript scope
- Understand what Asynchronous JavaScript is
- Ability to use JavaScript console
- Understand what the jQuery library is and when to use it

## Challenge(s)

- [Build a form validator script](https://github.com/iO-Academy/twbs-form)
  - Able to validate required fields
  - Able to change field required state depending on other fields state
  - Able to prevent numbers submitting in letter only fields
  - Able to prevent letters in number fields
  - Able to validate string lengths
  - Must display appropriate error messages and prevent form submission
  - No plugins! (including no jQuery)

## Programme

- What is JavaScript/ECMAScript?
	- [Where did they come from?](https://auth0.com/blog/a-brief-history-of-javascript/)
	- What is it used for?
	- How does it work
	- JS syntax
		- Variables
			- `var`, `let`, `const`
			- Scope difference
		- Conditionals
		- Loops
		- functions
			- named, anon, fat arrow
			- Anonymous vs named functions scope
			- default params
		- Reserved words
			- http://www.w3schools.com/js/js_reserved.asp
	- The JS console
		- ```console.log()``` 

- Using JavaScript on a webpage
	- inline script tags
	- external Javascript files
	- Script placement in a HTML file
		- http://stackoverflow.com/questions/436411/where-is-the-best-place-to-put-script-tags-in-html-markup
	- [Script async & defer](https://www.w3schools.com/tags/att_script_async.asp)
		- [async vs defer](http://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html)
	- [EXERCISE] Link a JS file to a HTML file, use a console.log() to verify that it worked correctly

- JavaScript data types
	- https://code.tutsplus.com/courses/javascript-fundamentals/lessons/data-types
	- EVERYTHING IS AN OBJECT!
	- When an object is not an object
	- typeof
	- parseInt()

- Interacting with the DOM
	- Selecting elements
		- `querySelector`
		- `querySelectorAll`
		- Old style: by Id, by class, by tag, by name
	- Manipulating elements
		- http://www.w3schools.com/js/js_htmldom_html.asp
	- Getting/Setting Data
		- [HTML5 data attributes](http://html5doctor.com/html5-custom-data-attributes/)
	- [EXERCISE] - Create an array of objects containing a name and age. Output each persons name in a `<p>` with their age as a data attribute.

- Handling DOM/browser events
	- http://www.w3schools.com/js/js_htmldom_events.asp
	- Inline HTML event handlers - DO NOT USE!
	- Assigning event handlers to the DOM
		- Creating event handler on an element that does not exist
		- Preventing the default action
		- Bubbling
	- http://www.w3schools.com/jsref/dom_obj_event.asp
	- [EXERCISE] Alert the persons age when clicking on their name from previous exercise.
	
- Working with data in JavaScript
	- Different data formats
		- https://www.w3schools.com/js/js_json_intro.asp
		- XML
		- JSON
	- Manipulating data
		- XML: https://www.w3schools.com/xml/xpath_syntax.asp
		- JSON:
			- https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify
			- https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse
	- [EXERCISE] Produce a JSON object of fields from https://github.com/iO-Academy/json-form
	
- AJAX
	- [Fetch](https://davidwalsh.name/fetch)
	- [EXERCISE] Use the JSON object created in previous exercise to practise sending data to the POST file
	
- Callbacks
	- What is a callback?
		- http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/
	- [EXERCISE] Write a function that adds two parameters together, then logs the results from a callback
- Useful functions
	- [map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
	- [filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
	
- Advanced Scope
	- Lexical scope: Function level with top down inheritance and hoisting
		- additional reading: http://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope/
	- this
		- refers to the current scope except when it doesnt
		- Functions: Anonymous vs fat arrow
		- http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/
	
- Prototype
- [JS errors](https://www.w3schools.com/js/js_errors.asp)
	- Error Types
	- Try, Catch, Finally
	- Custom Errors & Throw
	
- Window timers
	- http://www.w3schools.com/jsref/met_win_settimeout.asp
	- http://www.w3schools.com/jsref/met_win_setinterval.asp
	- [EXERCISE] Use setTimeout to display a newsletter signup modal after 10 seconds using the [example repo](https://github.com/iO-Academy/newsletter-signup-example)
	
- The event loop
	- [Video](https://dev.io-academy.uk/resources/js/the-event-loop.mp4)
		- [G Drive link](https://drive.google.com/drive/u/0/folders/14PnSHwuipK7Z_DLp4rH6BlibXZvIMu4P)
	- [Article](https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf)

- jQuery
	- https://api.jquery.com/
	- What is jQuery?
	- jQuery [http://api.jquery.com/on/] [http://api.jquery.com/trigger/]
	- Syntax
	- Differentiating jQuery variables
	- [Animation](http://api.jquery.com/animate/)
		- .animate()
		- .stop()
		- .fadeIn()/.fadeOut()/.fadeToggle()
		- .slideUp()/.slideDown()/.slideToggle()
		- [Velocity](http://velocityjs.org/)
		- [EXERCISE] Create a hamburger menu that slides in and out


- [Want more practise?](https://www.frontendmentor.io/challenges)
- [Additional Reading](http://jstherightway.org/)
- [more additional reading](https://blog.sessionstack.com/how-javascript-works-event-loop-and-the-rise-of-async-programming-5-ways-to-better-coding-with-2f077c4438b5)
- [For Fun](https://www.destroyallsoftware.com/talks/wat)

* * *
