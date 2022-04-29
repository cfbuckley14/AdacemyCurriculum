# Module 8 - Node.js

## Objectives

- Understand what Node.js and Express are
- Able to connect to a database from a Node app
- Understand and use MongoDB
- Understand common Node application architectures
- Able to implement a modular Node architecture

## Challenge

- Create an NPM module, with unit tests and demonstrate using it
	- Ask for suggestions if dont know what to build

## Programme

### [Node.js](https://nodejs.org/en/)

> Node.js is a JavaScript runtime. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient.

 - What is Node?
 > A JavaScript runtime environment and a library

 - Why Node?
 > Its JavaScript, it's FAST!

 - How Node?
 	- [Install node](https://nodejs.org/en/)
 	- type ```node``` on command line to test if working
	- [EXERCISE] Create a node server on port 3000 and output hello world (code-along)

- [Nodemon](https://nodemon.io/)
	- For auto-restarting node server
	- Install: `npm install -g nodemon`
	- Useage: `nodemon app.js`
	
- [NPM](https://www.npmjs.com/)
	- Mangaging dependencies
		- [See a modules dependencies](https://npm.anvaka.com/#/)
	- [Semantic Versioning](https://semver.org/)

- [Express](http://expressjs.com/) 
	- What is it?
- [Basic Routing](http://expressjs.com/en/starter/basic-routing.html) with Express
	- [EXERCISE] Install express and recreate hello world app
- [Advanced Routing](http://expressjs.com/en/guide/routing.html#response-methods)
	- [Express route tester](http://forbeslindesay.github.io/express-route-tester/)
	- [Response Methods](http://expressjs.com/en/guide/routing.html#response-methods)
	- Request Data
		- req.query: data from GET URL
		- req.params: data from route placeholder
		- body parser (https://github.com/expressjs/body-parser#installation)
	- [EXERCISE]: Create a GET and a POST route that respond with different dummy JSON
- [Express template engines](https://github.com/expressjs/express/wiki?_ga=1.121534152.1556123827.1465830802#template-engines)
	- [EXERCISE]: Install [handlebars](https://github.com/ericf/express-handlebars#installation) and render a template file

- [Using Static files](http://expressjs.com/en/starter/static-files.html)

- Node with [MySQL](https://www.npmjs.com/package/promise-mysql)
	- Connecting
	- Querying
	- [Example](https://github.com/CodeFoodPixels/node-promise-mysql/blob/master/examples/connection/query.js)
	- [EXERCISE]: Build this [ecommerce store](https://dev.io-academy.uk/resources/robot_stores/homepage.png) using [this database](https://dev.io-academy.uk/resources/robot_stores/robot_stores.sql). Make each item links to an [individual item page](https://dev.io-academy.uk/resources/robot_stores/product_page.png).
		- Stretch: Create an add product page
		- Stretch 2: Make the category and character filters work

- [Node with MongoDb](https://docs.mongodb.com/master/tutorial/install-mongodb-on-os-x/?_ga=1.173522723.1030587401.1463998511#install-mongodb-community-edition-with-homebrew)
	- [Connecting](http://mongodb.github.io/node-mongodb-native/3.1/tutorials/connect/)
	- [Querying](http://mongodb.github.io/node-mongodb-native/3.1/tutorials/crud/)
	- ObjectID
	- [GUI](https://www.mongodb.com/try/download/compass)
	- [EXERCISE]: Swap the ecommerce build to using MongoDB
    		- Tip: To move a database from MySQL to Mongo, export the main table as CSV, in Compass the add data button has a import file option that accepts CSV.

- [Modules](https://nodejs.org/api/modules.html)
	- installing
	- requiring
	- [exporting](http://www.tutorialsteacher.com/nodejs/nodejs-module-exports)
	- Additional Reading: [Using modules in browsers](https://jakearchibald.com/2017/es-modules-in-browsers/)

- JS Unit Testing
	- Jest
	    - What is it?
	    - Why do we test JS?
	    - What do jest tests look like?
	        - ```
	            test('adds 1 + 2 to equal 3', () => {
                     expect(sum(1, 2)).toBe(3);
                 })
              ```
        - Assertions
            - toEqual()
            - toBe()
            - toBeNull()
            - toThrow()
            - toBeGreaterThan()
            - toContain()
            - toContainEqual()
            - not.toEqual()
		- Using describe() to group tests
		- Installing using `npm i jest`
		- Running tests using `npm run test`
		- [EXERCISE]: Code along: Install Jest into a blank project and test some JS functions 

- Architecture
	- Common patterns
		- Micro-modules
		- Controller/services
	- Router
	- Controller Layer
	- Service Layer
	- [See Example](https://github.com/iO-Academy/NodeAppArchitecture)

- [EXERCISE]: Refactor the ecommerce site to use one of the above application architectures

- Middleware
	- [What is it?](https://medium.com/@jamischarles/what-is-middleware-a-simple-explanation-bb22d6b41d01)
	- When to use it?
		- Auth
		- Permissions
	- [How to use it in Node?](https://expressjs.com/en/guide/using-middleware.html)

- [EXERCISE]:
	#### Option 1
	[EXERCISE]: Log the time and URL of all requests from a middleware function.

	#### Option 2
	[EXERCISE]: Build a user login that allows users to click from a product to a purchase page where they can entre their payment details. The payment page should not be accessible to unauthenticated users. The buy button should only be shown when logged in.

- JSON endpoints
	- `response.json()`
	- FE JavaScript lives in `public/js`
	- [EXERCISE]: Create a product modal in the ecommerce store app.
		- Create a Node endpoint that returns all available information about a single product as JSON
			- URL should be something like: `/products/:id`
		- Fetch the product data from the above endpoint when clicking on a product in the product listing page and display it in a modal, instead of opening a seperate page

- MonoRepo vs FE/BE split
	- What is a monorepo/monolith?
	- Modern application approach
	- Benefits of splitting FE/BE
	- [EXERCISE]: Build 2 applications:
		- An Express API with a single route that returns the names of the students in your class as JSON
		- A React app that fetches that data and displays it on a page in a list

- Additional Reading: 
	- [mongoose](https://www.npmjs.com/package/mongoose)
	
