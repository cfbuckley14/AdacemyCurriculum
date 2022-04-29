# Module 7 - MVC & PHP Frameworks

## Objectives

- Understand and use an MVC structure
- Understand what a REST API is and why we use them
- Understand and use a PHP Framework
- Recognise and understand other common design patterns and anti-patterns
- Understand CI and why we use it

## Challenge

Strictly 4 minute (maximum) presentation on:

- A design (anti)pattern. Points to talk about:
	- What problem does it solve?
	- Is it commonly used?
	- What is the compromise of using it?
	- Provide an example
- Be aware of time and making the presentation engaging

## Programme

- CV & Interview Workshop (1 day workshop)

- MVC
	- What is it?
	- Why do we use it?
	- How do we use it?
	- Different ways to use it
	- [EXERCISE] Plan/Design an MVC structure for a todo app
	- [Additional Video on ADR](https://www.youtube.com/watch?v=GGMxzc8tpdY)

- PHP Frameworks
	- What are they?
	- Why do we use them?
		- consistency of code: enforces a single way per project
		- transferrable skills
		- routing
		- MVC/Architecture
		- Common usage is an API
		
- Introduction to Slim Framework [http://www.slimframework.com/]
	- [EXERCISE] Set up Slim locally
		- https://github.com/iO-Academy/slim4-skeleton

- Autoloading
	- Folder structure
	- [composer.json](https://github.com/iO-Academy/AcademyPortal/blob/master/composer.json)
	- `composer dump-autoload`
- Routing
	- .htaccess directing http requests to public/index.php
	- routes.php
		- [How to handle request](https://www.slimframework.com/docs/v4/objects/routing.html)
		- Get/Post
		- Url matching
		- The callback
			- $request, $response, $args
		- Outputting to the front end
- [EXERCISE]: Create a new route that returns a new static template file

- Dependancy Injection/Inversion of Control
	- What is it?
	- Why do we use it?
		- Pros:
			- Testability
			- Easier modification/maintainability
			- Decoupling
		- Cons:
			- User must instansiate all dependancies manually everytime
	- Try not to create objects inside other objects, just pass them in

- Factories
	- What are they?
		- Objects that create other objects with all of their dependancies (break DI to help you follow DI)
		- eg: audi car garage class example
		- Just has to be callable eg: a function or a class
		- dependancies.php to see anonymous function example
	- Why do we use them?
		- Prevents need for excessive instansiation
		- Ensures all dependancies are consitently created in the correct manner 
		- Encapsulation - Don't care how its made, just that it is

- Depandancy Injection Container (DIC)
	- What is it?
		- Essentially an array of pre-made objects and their dependancies
	- Why do we use it?
		- Groups all your factories into one place
		- Reduces code smell of too many constructor params
	- dependancies.php
		- [Making factories invokeable](https://github.com/iO-Academy/AcademyPortal/blob/master/src/Factories/AdminControllerFactory.php)
		- [Register in DIC](https://github.com/iO-Academy/AcademyPortal/blob/master/app/dependencies.php)
			- Container Key name does not need to match factory class name, this hides factories
		- [Using factories in routes.php](https://github.com/iO-Academy/AcademyPortal/blob/master/app/routes.php)
			- [What can be passed to a route](https://www.slimframework.com/docs/v4/objects/routing.html#container-resolution)

- Controllers in Slim
	- Skeleton app - anonymous function in routes.php
	- [Controller with a dependancy](https://github.com/iO-Academy/AcademyPortal/blob/master/src/Controllers/AdminController.php)
		- must be invokeable (to match routes.php)
			- Params are the $request, $response, $args (populated by slim)
		- Needs a factory thats registered in DIC
		- Allows use of controller via factory in routes.php

- [EXERCISE] - Convert your existing route to a callable that calls a factory from the DIC that returns instansiated controller with its dependancy (PHP Renderer). Use your controller to output the template file you created. 

- Views in Slim 
	- Where to put your static files
		- treat Public as a root for static eg: js, cs etc...
	- To respond with HTML: [PHP Renderer](https://github.com/slimphp/PHP-View#usage-with-slim-4)
		- dependancies.php puts it in DIC 
		- templates location declared in settings.php
		- if using in routes.php
			- `return $this->renderer->render($response, "/hello.php", $args);`
		- if using anywhere else remember to inject the depandancy to allow you to use $this->renderer
		- passing data to the view
			- $args is a associative array of the data you want in the view
			- the array keys become available as variables in your [template file](https://github.com/iO-Academy/AcademyPortal/blob/master/templates/registerUser.phtml)
	
	- To respond with [JSON](https://github.com/iO-Academy/AcademyPortal/blob/master/src/Controllers/RegisterUserController.php):
		- `$response->getBody()->write(json_encode($data));`
		- `return $response->withStatus($statusCode);`
		- Status code is optional (default is 200)
	
	- To respond with a redirect:
	```php
	return $response->withHeader('Location', './admin');
	``` 
	
	- To respond with a [status code](https://www.slimframework.com/docs/v4/objects/response.html#the-response-status):
		- Usually used for error codes where you dont want to send data

	- ViewHelpers
		- To abstract logic away from the HTML

- [EXERCISE]: Build a simple todo application using slim
	- [Example](https://github.com/mporam/slim-todo-app) (This is Slim 3)

- [REST](https://code.tutsplus.com/tutorials/a-beginners-guide-to-http-and-rest--net-16340) APIs 

	> Stateless (usually authenticated by dependant call, cookie, or digest authentication) calls via http verbs (put/get/post/delete) to create/retrieve/update data or execute functions with a consistent structured response in a consistent format.

	- Why use REST?
	- Stateless
		- How to do authentication?
		- Tokens
		- Additional Reading: [OAuth2](https://medium.com/@darutk/the-simplest-guide-to-oauth-2-0-8c71bd9a15bb)
	- URL structure
		- `/entity`
		- `/entity/{id}`
		- `/entity?filter={value}`
	- HTTP verb meanings
	- RESTful (sort of REST)
	- [Documenting your REST API - Example](https://gist.github.com/iros/3426278)
		- Additional reading: [Swagger](https://swagger.io/docs/specification/2-0/what-is-swagger/)

- CI
	- What is it?
	- Why do we use it?
	- Demo CircleCI for the portal
	- Show Github integration
	- Show Slack integration (#ci-builds)

- [Additional Reading](https://dev.to/charliedevelops/getting-started-with-slim-php-framework-by-building-a-very-simple-mvcoop-app-4j2b): Walkthrough of simple MVC OOP Slim Application (Slim 3 examples)
