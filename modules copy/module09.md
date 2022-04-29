# Module 9 - Industry Skills 

## Objectives
- Understand what GraphQL is and when to choose between it or REST
- Understand what Typescript is and why its used
- Use TypeScript with React
- Expand your knowledge of react with react libraries
- Use a language debugger
- Understand what TDD is and how to do it
- Finalise your CV and portfolio
- Practise technical tests

## Challenge

Create an account on [CodeWars](https://www.codewars.com/) (set your clan to iO Academy) and complete a 6kyu Kata

## Programme

- [GraphQL](https://graphql.org/)
	- A different approach to building APIs
	- What is it?
	- Why use it?
	- Operation types
		- Queries
		- Mutations
		- Subscriptions
	- Documenting GraphQL APIs
		- [graphql-docs](https://www.npmjs.com/package/graphql-docs)
	- [Example API](https://github.com/iO-Academy/graphql-course-api-example)
	- [EXERCISE]: Build a page that displays the following info about the next SpaceX Launch using [this API](https://api.spacex.land/graphql/)
		- Full name of the launch location
		- Launch date in the following format: DD/MM/YYYY HH:MM
		- Name of the rocket

- React
	- [Routing](https://codeburst.io/getting-started-with-react-router-5c978f70df91)
		- react-router-dom
		- Route matching with `<Route>`
		- History
		- `<Switch>`
		- Navigation with `<Link>`
		- ```import { Route, Switch, Link } from 'react-router-dom'```
		- [EXERCISE] Create a navbar that has Home, About, Contact Us components

	- [Containment](https://reactjs.org/docs/composition-vs-inheritance.html#containment)
		- Using `props.children` to nest components
		- When to use it

	- [Context API](https://www.smashingmagazine.com/2020/01/introduction-react-context-api/)
		- What is it?
		- How and when it's used

	- Class Components
		<details>
		<summary>Example</summary>
	
		```jsx
		class Example extends React.Component {
			constructor(props) {
			    super(props);
			    this.state = {
				count: 0 // default state
			    }
			}

			render() {
			    return (
				<div>
				    <p>Hello, I'm a Class component!</p>
				    <p>{this.state.count}</p>
				    // change state with setState function
				    <button onClick={() => this.setState({ count: this.state.count + 1 })}>
					Click me
				    </button>
				</div>
			    )
			}
		}
		```
		</details>

		- Before Hooks were released in 16.8.0, class components managed state
		- Functional components existed only for stateless components
		- This style of React is being phased out but worth being aware of
		- Additional reading: Using [lifecycle](https://reactjs.org/docs/react-component.html) in class components

- [TypeScript](https://www.typescriptlang.org/)
	- What is it?
	- Syntax
		- variable definitions
			- `let foo: string = 'mike'`
		- param and return types
			- `function bar(baz: string): number {}`
	- [Available types](https://www.typescriptlang.org/docs/handbook/basic-types.html)
		- boolean, string, number, Array<internals>, any, void
	- [Interfaces](https://www.typescriptlang.org/docs/handbook/2/objects.html)
	- [Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html)
	- DOM types
		- [HTML Element Types](https://microsoft.github.io/PowerBI-JavaScript/interfaces/_node_modules_typedoc_node_modules_typescript_lib_lib_dom_d_.htmlelementtagnamemap.html)
		- [Event Types](https://microsoft.github.io/PowerBI-JavaScript/interfaces/_node_modules_typedoc_node_modules_typescript_lib_lib_dom_d_.htmlelementeventmap.html)
	- Compiling TS
	- [EXERCISE]: Build a page which tells you how old you are on different planets, when given an age in Earth years. Using the below figures:
		- Mercury: 1 year = 0.2408467 Earth years
		- Venus: 1 year = 0.61519726 Earth years
		- Mars: 1 year = 1.8808158 Earth years
		- Jupiter: 1 year = 11.862615 Earth years
		- Saturn: 1 year = 29.447498 Earth years

- TypeScript with React
	- [Getting started](https://create-react-app.dev/docs/adding-typescript/)
	- [Components & props](https://github.com/typescript-cheatsheets/react/blob/main/README.md#function-components)
	- [Hooks](https://github.com/typescript-cheatsheets/react/blob/main/README.md#hooks)
	- [Child component types & prop types](https://github.com/typescript-cheatsheets/react/blob/main/README.md#useful-react-prop-type-examples)

- Styling components
	- Utility Libraries
		- [Tailwind CSS](https://tailwindcss.com/)
	- UI Libraries
		- [Bootstrap](https://react-bootstrap.github.io/getting-started/introduction/)
		- [Material UI](https://material-ui.com/)
		- [Tailwind UI](https://tailwindui.com/documentation)
	- [EXERCISE]: Create a registration form with a email input, DOB date picker, favourite colour select dropdown and submit button using a UI library or tailwind CSS
	- [Styled-components](https://styled-components.com/)


- React Architecture
	- [Atomic Design](https://atomicdesign.bradfrost.com/chapter-2/)
		- What is it?
		- How does it work?
			- Atoms
			- Molecules
			- Organisms
			- Templates
			- Pages
		- Recommended folder structure
		- Additional reading: [Atomic Design Tooling](https://atomicdesign.bradfrost.com/chapter-3/)
	- React best practices
		- Create [common modules](https://alexkondov.com/tao-of-react/#create-a-common-module) at the start
		- [Wrap external components](https://alexkondov.com/tao-of-react/#wrap-external-components)
		- [Use component folders](https://alexkondov.com/tao-of-react/#move-components-in-folders)
		- [Debugging react](https://reactjs.org/docs/strict-mode.html)
	- [EXERCISE]: Build a basic visual metronome with a start stop button and a set pace, using a UI library and following Atomic design
		- Stretch goal: Add different set paces available to choose from

- TDD: Test Driven Development
	- [What is it and why do we do it?](https://medium.com/@MasterOfCodeGlobal/benefits-of-test-driven-development-64a24bbe743e)
	- Red, Green, Refactor
		- Demo a maths function
	- Realistic application. Start something, then every future function apply TDD
	- [EXERCISE] Use TDD to [complete this coding exercise](https://github.com/iO-Academy/FST-curriculum/blob/master/tdd-exercise.md)
	- [Additional Practice](https://cyber-dojo.org/dojo/index/)

- Debugging
	- Logging
		- JavaScript - not just `console.log`: [Console API](https://levelup.gitconnected.com/moving-beyond-console-log-8-console-methods-you-should-use-when-debugging-javascript-and-node-25f6ac840ada)
		- PHP - not just `var_dump`: [PHP Debugging](https://www.codebyamir.com/blog/php-debugging-varexport-vardump-printr)
			- Expanding `var_dump`: [__debuginfo](https://www.php.net/manual/en/language.oop5.magic.php#object.debuginfo)
	- [JavaScript Debugger](https://www.w3schools.com/js/js_debugging.asp)
		- Other debuggers: [xdebug](https://xdebug.org/)
	- Breakpoints
		- Stepping
			- Step Over: Run next line of code in current scope
			- Step In: Go to first line in current sub-function call
			- Step Out: complete current function and go to next line of code after current function call
		- `debugger`
			- Example:
			```javascript
			function sum(a,b) {
				var c = a + b;
				debugger;
				return c;
			}
			```
	- [EXERCISE] Fix [this code](https://github.com/iO-Academy/JavaScript-Diamond-Bug) using the JS debugger.
		- Bonus points if you find the boat!

- Job application preparation
	- Finish your CV & have it reviewed
	- Finish your portfolio
	
- Technical test practice
	- [EXERCISE]: Practise some of the below technical tests, speak to your trainer about which kinds you should focus on, or do a selection of all of them.

### Code Katas
	
- [HackerRank](hackerrank.com/)
	- [Problem-solving](https://www.hackerrank.com/domains/algorithms)
	- [Data Structures](https://www.hackerrank.com/domains/data-structures)
	
- [CodeWars](codewars.com/)
	- [Katas](https://www.codewars.com/kata/search/my-languages?q=&r[]=-8&r[]=-7&r[]=-6&beta=false&order_by=popularity%20desc)
		- If you can complete a few 6kyu, try a 5
	
- [LeetCode](https://leetcode.com/)
	- [Top interview questions](https://leetcode.com/problemset/all/?listId=wpwgkgt)
	
- [Cyber Do-Jo](https://cyber-dojo.org/creator/home)
	- [These are a bit harder](https://cyber-dojo.org/creator/choose_problem?type=single)
	
### Whiteboarding
	
You can do these in pairs or alone, either way, ask your trainer to review after. Psuedo code/explain the following applications/things:
- A shopping basket in an ecommerce store
	- Must be able to add and remove items
	- Must be able to specify quantity of each item and change that quantity
- A user registration form
	- Should store data in a database
	- Should validate the data
- What happens when you type a web address into a browser window
	- Explain the steps in as much detail as you can
	
	
### Take home tasks
	
- [Convert numbers to roman numerals (4hrs)](../exercises/roman-numerals.md)
- [Create a decryption page (4hrs)](../exercises/decryption.md)
- [Create a UK PAYE income tax calculator (6hrs)](../exercises/income-tax.md)
- [Build a sunrise calculator (8hrs)](../exercises/sunrise-calculator.md)
