# Module 2 - Intro to Programming

## Objectives

- Understand the syntax and structural elements of PHP
- Know how to correctly apply the various control-flow structures
- Understand PHP data types, type-juggling, and operator precedence
- Understand the DRY principle
- Understand what an SQL database is
- Ability to efficiently query a database
- Use a database from PHP

## Challenge
- [Post / poles challenge](https://docs.google.com/document/d/1VhK6-YU9sMh5IMELMWi4p4bbfZyXjIQL1ZZCy3N3h9g/edit)

## Programme
- What is PHP?

- LAMP
	- What is LAMP?
	- PHP's role in LAMP?
	- Virtual Machines
	- Vagrant
		- What is it?
		- `vagrant up`
	- Docker
		- What is it?
		- [Docker Image](https://github.com/iO-Academy/docker-image)
		- `docker ps` : list running containers
		- `docker-compose up -d` : turn container on. `-d` sets to background process.
		- `docker exec -it {container ID} bash` : enter container using bash
		- `docker-compose stop` : shutdown container
		- `docker-compose restart` restart container
		- `docker-compose down` destroy container

- PHP Storm
	- [EXERCISE]: Sign up to a jetbrains account using your [Github education student developer pack](https://education.github.com/pack/offers#jetbrains) and sign into your account in PHPStorm
	- [Shortcuts](https://resources.jetbrains.com/storage/products/phpstorm/docs/PhpStorm_ReferenceCard.pdf)
	- [Further reading](http://manovotny.com/phpstorm-keyboard-shortcuts/)

- Password Managers
	- Secure password storage and password generation
	- [LastPass](https://www.lastpass.com/)
		- [Firefox Addon](https://addons.mozilla.org/en-GB/firefox/addon/lastpass-password-manager/)
		- [Chrome Extension](https://chrome.google.com/webstore/detail/lastpass-free-password-ma/hdokiejnpimakedhajhdlcegeplioahd)
	- [Haveibeenpwned](https://haveibeenpwned.com/)
		
- Intro to basic language constructs of PHP
	- What is PHP? 
		- php.ini
		- ```phpinfo()``` 
		- [EXERCISE] Write a hello world program
	- Syntax 
	    - keywords, formatting
		    - [PSR12](https://www.php-fig.org/psr/psr-12/)
	    - examples of syntax in different languages
		    - [Rosetta Code](http://rosettacode.org/wiki/99_Bottles_of_Beer)
	    - syntax vs semantics
	    
	> The term syntax refers to grammatical structure whereas the term semantics refers to the meaning of the vocabulary symbols arranged with that structure. Grammatical (syntactically valid) does not imply sensible (semantically valid), however.
	- Variables 
		- What is a variable?
		- Allowable names
		> Variable names follow the same rules as other labels in PHP. A valid variable name starts with a letter or underscore, followed by any number of letters, numbers, or underscores. As a regular expression, it would be expressed thus: ```'^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*' ```
	
	- Constants 
		- ```define("PI", 3.1415927);```
		
		>__Differences between constants and variables are:__
	    > - There is no need to write a dollar sign ($) before a constant, whereas in a variable one has to write a dollar sign.
	    > - Constants cannot be defined by simple assignment, they may only be defined using the define() function.
	    > - Constants may be defined and accessed anywhere without regard to variable scoping rules (unless in a class).
	    > - Once the constants have been set, they may not be redefined or undefined.

	- Data Types 
		- ```String; Integer; Float; Boolean``` 
		- Typed Languages
		- [Static/dynamic type checking](http://php.net/manual/en/function.gettype.php)
		- Type juggling & type casting
		- var_dump()

	- [Strings](http://php.net/manual/en/language.types.string.php)
		- Single vs double quotes
		- "Variable Interpolation" 
		- Special Characters 
		- ```"\n; \t; \\"``` 
		- Concatenation
		- echo
	
	- [EXERCISE] 
		- Create a selection of variables and constants to represent at least one example of each data type, and output these using echo and var_dump. Using single and double quotes prove variable interpolation. Finally, create a variable that doesn't work based on the info you have about allowed names. 
	- Operators 
		- Assignment ```=```
		- Mathimatical ```* / + - %```
		- Comparison ```== === != !== > >= < <= <=>```
		- Compound assignment ```*= /= += -= .=```
		- Increment/decrement ```++ --``` 
		- Logical ```! && ||```
			- [Google Doodle - George Boole](https://www.google.com/doodles/george-booles-200th-birthday)
			
	- Precedence 
		- [Operator Precedence](http://www.php.net/manual/en/language.operators.php) 		

	- Conditionals
		- if
		- if ... else
		- elseif
		- switch
		- coding style (PSR)
		- [Ternary Operator](https://davidwalsh.name/php-shorthand-if-else-ternary-operators) ```(<condition>) ? <value if true> : <value if false>;```
			- `?:`
			- `??`
	
	- [EXERCISE]
		- Generate a [random number](https://www.php.net/manual/en/function.rand.php) and create a conditional statement to display two possible values depending on the random number. E.g. Heads & Tails.
	- Arrays
		- Indexed arrays (Numeric, Enumerative)
		```
		$days_array = ['Mon', 'Tues', 'Wed', 'Thurs', 'Fri', 'Sat', 'Sun'];
		 ```
		- Associative arrays
		```
		$personal_details = ['Name' => 'John Doe', 'Age' => 21, 'Sex' => 'Male'];
		``` 
		- key / value
		- Multi-dimensional arrays
		
	- Working with Arrays
		- Adding to arrays
		- Iterating through arrays 
		```
		foreach ($array as $value) {...}
		```
		- [Array Functions](http://php.net/manual/en/ref.array.php)
	- [EXERCISE]
		- From this array `[1, 2, 3, 4, 5, 6, 7, 8]` add 9 & 10 to it using 2 different methods
		- Randomise the contents of the array using an array function
		- Iterate through this array and output odd values
	- Loops
		- [for](https://www.w3schools.com/php/php_looping_for.asp)
		- [while](https://www.w3schools.com/php/php_looping.asp)
		- [foreach](https://www.w3schools.com/php/php_looping_for.asp)
		- continue / break
		- Nested loops

- Functions
	- [Functions](http://php.net/manual/en/functions.user-defined.php) 
		- Declaring Functions 	
		- Parameters
			- Type hinting
		- Optional Parameters
		- Return values
			- [Return typing](http://php.net/manual/en/functions.returning-values.php#functions.returning-values.type-declaration)
	- [PHP Built in Functions](http://php.net/manual/en/functions.internal.php) 
		- Maths functions
		- String Functions
		- Array Functions
		```
		is_array(), array_key_exists(), array_slice(), array_splice()
		```
		- Pass by reference

- Comments 
	- Single line
	- Multi line
	- Standard formats e.g DocBlocks
	
	- [EXERCISE]
		- Create a function that takes a number and multiplies it by itself and adds the second parameter then returns the value. Second parameter must default to 0. Ensure it is correctly commented. 


- Problem solving
	- How do you solve a problem?
	- Pseudocode
		- What is the problem?
		- What is the expected input/output?
		- What are the steps required to get from input to output
		- Use Google!
		- Demo: Remove names starting with 'A' from this list: `'Alice,Oliver,Robbie,Mike,Audrey,Anton,Lucy,Charlie,Chris'`
	- How to read/use the php manual

- [EXERCISE] Blackjack
	- create a basic blackjack game based on the example
		- [Show example](https://github.com/iO-Academy/BlackJack)

**Working with Databases**
- [Use this for mock Data](https://www.mockaroo.com/)

- Introduction to Databases
	- What is a database?
	- What is SQL?
	- Why do we use a database
	- What is MySQL

- Interacting with a database
	- [Command Line](https://www.digitalocean.com/community/tutorials/a-basic-mysql-tutorial)
	- GUI ([Sequel Pro](http://www.sequelpro.com/))

- Introduction to SQL
	- Entities 
		- Database
		- Table
		- Field
		- Index
		- [Functions](http://dev.mysql.com/doc/refman/5.7/en/functions.html)
	- Data Types
    	- Numeric Types
    	- String Types
    	- Date & Time Types
    	- Other Types
    	- [EXERCISE]: Create table to store local businesses using relevant data types
    - SQL Syntax
    	- Data Manipulation Language (DML)
    		- SELECT
    			- AS
    			- WHERE
    			- GROUP BY
    			- ORDER BY | ASC | DESC
    			- LIMIT
    		- JOIN
    			- LEFT | RIGHT
    			- INNER
    			- There are others but these are the ones you need
    		- INSERT
    		- UPDATE
    		- DELETE
    	- [Additional Reading](http://stackoverflow.com/questions/2905292/where-vs-having) WHERE vs HAVING
    
    - [EXERCISE 1: SELECT, JOIN & INSERT]: From [this DB](https://dev.io-academy.uk/resources/exercises1.sql) write queries that:
        - Grabs all the Adult names along with their DOB's.
        - Grabs all the Adults names along with their Children's names.
        - Add a new colour.
        - Add a new child that has your newly created colour as their favourite.
        - [Bonus extra]: Find the most commonly occurring favourite colour.
    
    - Prepared Statements & PDO
    	- Using PDO
    	- PREPARE Statements
    	- [SQL Injection](http://www.w3schools.com/sql/sql_injection.asp)
    	- EXECUTE 
    	- [EXERCISE 2: PDO]: Pull the data out of [this](https://dev.io-academy.uk/resources/MailMerge.sql) DB and output in a list on the front end
    
    - Indexes
    	- Primary Keys
    	- [UNIQUE](http://www.w3schools.com/sql/sql_unique.asp)
    	- [Foreign Keys](http://www.w3schools.com/sql/sql_foreignkey.asp)
    	
    - [Functions](https://www.w3schools.com/sql/sql_ref_mysql.asp)
    	- COUNT
    	- AVG
     
    - Adv. WHERE
    	- [LIKE](http://www.w3schools.com/sql/sql_like.asp)
    		- [Wildcards](http://www.w3schools.com/sql/sql_wildcards.asp)
    	- [BETWEEN](http://www.w3schools.com/sql/sql_between.asp)
    
    - Advanced Concepts
    	- Transactions
    	- Relationship Types
    		- One-to-One
    		- One-to-Many
    		- Many-to-Many
	- EAV Tables (Entity–attribute–value)
    
    - Other Databases
    	- [Graph DBs](https://drive.google.com/file/d/0B0PXaYz86jzXLVRKX09LeHRvZjg/view?usp=sharing&resourcekey=0-axmTMsiyU2jB7oC2xVId2g)
    	- Additional Reading: 
    		- [NoSQL](https://www.youtube.com/watch?v=qUV2j3XBRHc)
    		- [SQL ZOO](https://sqlzoo.net/)


