
# Module 6 - Advanced Programming Principles

## Objectives

- Introduction to design patterns and anti-patterns
- Understand SOLID and DRY
- Understand how to utilize regular expressions
- Build a simple OO class hierarchy
- Unit test a OO file
- Work with exceptions and error handling (try catch etc.)

## Challenge

Prints the numbers 0-1000-0 (every number inbetween), with 1000 only once and each number on a new line in:

1. The fewest PHP characters you can
2. A unique way that no other team members have used

## Programme

- Recapping Key concepts from 1st PHP Module
	- Data Types
		- Loose vs Stongly typed languages
		- Type checking (Static/Dynamic)
		- Type casting
		- Type juggling
	- Quotes - single, double quotes, concatenation
	- Comments - single line, multiline, docblocks
	- Arrays
		- Numeric, Associative, Multi-dimensional
		- More Array Functions
			- is_array(), count(), in_array(), array_key_exists(), array_merge()
		- Callbacks: array_map(), array_filter()
		- [EXERCISE]: Create a script which will take a string and analyse it to produce the following stats:
			- Number of characters
			- Number of words
			- Number of sentences
			- Number of paragraphs
			- Longest word
			- Average sentence length
	- Operators
		- Assignment
		- Mathematical
		- String
		- Comparison
		- Logical
		- Precedence and Definitions
	- Conditionals and Loops
		- if
		- if ... else
		- elseif
		- switch
		- ternary operator
		- foreach
		- for
		- while
		- continue / break
	- Functions
		- Naming
		- Parameters
			- Optional/Default values
		- Return
		- Lambda / Anonymous Functions
	- [String Functions](http://php.net/manual/en/ref.strings.php)
		- [substr()](http://php.net/manual/en/function.substr.php)
		- [str_shuffle()](http://php.net/manual/en/function.str-shuffle.php)
		- [trim()](http://php.net/manual/en/function.trim.php)
		- [ltrim()](http://php.net/manual/en/function.ltrim.php)
		- [rtrim()](http://php.net/manual/en/function.rtrim.php)
		- [explode()](http://php.net/manual/en/function.explode.php)
		- [implode()](http://php.net/manual/en/function.implode.php)
		- [htmlentities()](http://php.net/manual/en/function.htmlentities.php)
		- [strpos()](http://php.net/manual/en/function.strpos.php)
 
 - [Regular Expressions](https://regex101.com/)
	- [Quick Start Regex](http://www.regular-expressions.info/quickstart.html)
  	- Characters and Symbols
  	- RegEx Functions
		- [preg_match()](http://uk1.php.net/manual/en/function.preg-match.php)
    		- [preg_match_all()](http://uk1.php.net/manual/en/function.preg-match-all.php)
  	- [Pattern Modifiers](http://php.net/manual/en/reference.pcre.pattern.modifiers.php)
  	- [EXERCISE]: Write a PHP Script that can match the following patterns
  		- An email address
		- A English postcode
		- The amount of occurances of 'bacon' in the following text
			> Spicy jalapeno bacon ipsum dolor amet kevin buffalo frankfurter, sausage jerky pork belly bacon. Doner sausage alcatra short loin, drumstick ham tenderloin shank bresaola porchetta meatball jowl ribeye ground round. Ribeye pork loin filet mignon, biltong shoulder short ribs tongue ball tip drumstick ground round rump pork chop. Kielbasa bacon strip steak andouille ham short ribs short loin venison frankfurter spare ribs doner corned beef.
	- [filter_var](https://www.php.net/manual/en/function.filter-var.php)
		- [Validate filters](https://www.php.net/manual/en/filter.filters.validate.php)
		- [Sanitize filters](https://www.php.net/manual/en/filter.filters.sanitize.php)
 
- Language Concepts and Configuration
  - Including Files
    - include / include_once
    - require / require_once
  - [Globals](http://php.net/manual/en/language.variables.scope.php) + [$GLOBALS](http://php.net/manual/en/reserved.variables.globals.php)
  - References / passing by reference
  - File System Basics
    - fopen, fread, fclose
    - file_get_contents, file_put_contents etc.
    - performance
  - .htaccess files
  	- [Additional Reading](http://www.htaccess-guide.com/)

- OOP
  - Classes & Objects Recap
    - What is a class / object?
    - syntax
    - Class properties / methods
	    - `this`
    - [Visibility (PPP)](http://www.php.net/manual/en/language.oop5.visibility.php)
    - setters / getters
  - Constructor
    - __construct()
  - Inheritance 
  - [Static Context](http://php.net/manual/en/language.oop5.static.php)
  	- `self`
  	- [Additional reading: Late Static Binding](http://www.codeproject.com/Articles/853792/A-walk-through-into-Late-Static-Binding-in-PHP)
  - Hydrators & Entities
    - [EXERCISE] Create a DB entity class and hydrate it from another class using a static method
  - [Magic Methods](http://php.net/manual/en/language.oop5.magic.php)
  - [Interfaces](http://php.net/manual/en/language.oop5.interfaces.php) & [Abstracts](http://php.net/manual/en/language.oop5.abstract.php)
	- Polymorphism
  - Overriding Methods
  	- [parent](http://php.net/manual/pl/keyword.parent.php)
	- [final](http://php.net/manual/en/language.oop5.final.php)
	- [EXERCISE]: Create a barn object and store at least 3 different kinds of animal objects in it
  - [SOLID](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
  	- [Additional Reading](https://dev.to/evrtrabajo/solid-in-php-d8e)
  - [Namespaces](https://daylerees.com/php-namespaces-explained/)
	- [namespace keyword and __NAMESPACE__ constant](http://php.net/manual/en/language.namespaces.nsconstants.php)
  - Autoloading
  	- [composer autoloading](http://phpenthusiast.com/blog/how-to-autoload-with-composer)
  - [Exceptions](http://php.net/manual/en/language.exceptions.php)
  	- [PHP Errors](http://php.net/manual/en/errorfunc.constants.php)
  - [Design Patterns](https://sourcemaking.com/design_patterns) & [Anti-patterns](https://sourcemaking.com/antipatterns)
  	- [Value-object pattern](https://kacper.gunia.me/ddd-building-blocks-in-php-value-object/)
	- [Adaptor pattern](https://sourcemaking.com/design_patterns/adapter/php)
	- [Singleton](https://sourcemaking.com/design_patterns/singleton)
	- [God Class](https://sourcemaking.com/antipatterns/the-blob)
	- [Golden hammer](https://sourcemaking.com/antipatterns/golden-hammer)
	- [Additional Reading](https://www.tutorialspoint.com/design_pattern/design_pattern_overview.htm)

- Unit Testing
	- [Mocking/Stubs](https://phpunit.de/manual/current/en/test-doubles.html#test-doubles.stubs)

- Server Communication
  - [HTTP Headers](https://code.tutsplus.com/tutorials/http-headers-for-dummies--net-8039)
  - [HTTP status Codes](https://httpstatuses.com/)
  	- For fun: [HTTP Status Dogs](https://httpstatusdogs.com/)
  - [Browser Caching](http://www.makeuseof.com/tag/browser-cache-makeuseof-explains/)
  - Cookies
  - Sessions
  - [cURL](https://www.php.net/manual/en/curl.examples-basic.php)

