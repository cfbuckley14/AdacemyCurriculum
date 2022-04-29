# Module 5 - Front-end Tools

## Objectives

- Able to animate things with CSS
- Understand and use a CSS preprocessor
- Able to demonstrate use of a CSS framework
- Understand the importance of accessibility and how we can improve it
- Able to use browser APIs
- Understand what React is and be able to build an app with it

## Challenge

#### Build a finance calculator that accepts:
- The amount you would like to borrow (£)
- Your expected annual salary (£): default £25,000
- Monthly repayment percentage: default/minimum 10%

The calculator should tell you how much you will repay each month and long it will take you to pay off the loan, in years and months. If the final payment is less than the others, it should tell you the final payment amount.

*Requirements:*
- Borrow amount between £1 and £10,000
- Must be written in React
- Must use a CSS preprocessor

*Example:*
- https://dev.io-academy.uk/resources/finance-calc/
- DO NOT LOOK AT THE CODE

## Programme

- [SVG](https://www.w3schools.com/graphics/svg_intro.asp)
    - [Icon fonts](https://icomoon.io/app/#/select)
        - HTTP Overhead benefits
    - [EXERCISE]
        - Option 1: Build a simple solar system using SVG - [Example here](https://dev.io-academy.uk/resources/solar.png)
        - Option 2: Build a pong game - [Example here](https://codepen.io/mporam/full/MWvOOQY)
        - Option 3: Build a snake game - [Example here](https://codepen.io/mporam/full/YzxEYMm)

- [CSS Animations](http://www.w3schools.com/css/css3_animations.asp)
    - [EXERCISE:]
        - Option 1: Make your svg planets orbit the sun - [Example](https://codepen.io/mporam/full/KjvMOX)
        - Option 2: Make pong auto-play - [Example](https://codepen.io/mporam/full/QWMOOrX)
        - Option 3: Make snake auto-play - [Example](https://codepen.io/mporam/full/MWvOrRr)
    
- [CSS Frameworks](http://usablica.github.io/front-end-frameworks/compare.html)
    - What are they?
    - Why?
    - Grid systems
    - [Bootstrap](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
    - [EXERCISE:] Build [this site](https://htmlpreview.github.io/?https://raw.githubusercontent.com/iO-Academy/bootstrap-hosting-site/main/index.html), make it responsive. (don't look at the code)

- CSS preprocessors
    - [Sass](http://sass-lang.com/)
    - Compiling
    - [EXERCISE:] Convert your portfolio build to using Sass

- APIs
    - What are they?

- [Postman](https://app.getpostman.com/app/download/osx64)

- Browser APIs
    - Mobile APIs
    - [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
        - [Blog post](https://davidwalsh.name/promises)
    - [async & await](https://davidwalsh.name/async-await)

- Accessibility
    - [WCAG](https://www.w3.org/TR/WCAG21/)
        - [Principles of accessiblity](https://www.w3.org/WAI/fundamentals/accessibility-principles/)
        - [Conformance levels](https://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html)
            - [webaim checklist](https://webaim.org/standards/wcag/checklist)
            - [Essential accessibility checklist](https://kma.global/wp-content/uploads/2019/07/WCAG_2.1_Checklist.pdf)
    - [Evaluation tools](https://www.w3.org/WAI/ER/tools/)
        - [Contrast checker](https://webaim.org/resources/contrastchecker/)
        - [ChromeVox](https://chrome.google.com/webstore/detail/chromevox-classic-extensi/kgejglhpjiefppelpmljglcjbhoiplfn)
        - *More to come!*
    - [ARIA tags](https://developers.google.com/web/fundamentals/accessibility/semantics-aria)

- React
    - What is it

  > React is a declarative, efficient, and flexible JavaScript library for
  building user interfaces. It lets you compose complex UIs from small
  and isolated pieces of code called “components”.

  or

  > React is a library to help you build modular interfaces for web applications

    - [The Docs](https://reactjs.org/docs/getting-started.html)

- We are learning core react
    - Browser support

- [The Virtual DOM](https://www.codecademy.com/articles/react-virtual-dom)
    - react vs react-dom

- Create-react-app
  - Front-end build tools
    - [webpack](https://webpack.js.org/)
```bash
npx create-react-app my-app
cd my-app
npm start
```
- [Built in functionality](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)

- [EXERCISE] Use the create react app and get a react app running locally

- Components
  ```jsx
  const Greeting = () => <h1>Hello, I’m a functional component!</h1>

  export default Greeting
  ```
	- Functional because they are basically functions
	- Stateful because they can hold and/or manage local state
	- Smart because they can contain logic
	- Container because they usually hold/contain numerous other components

- Using a Component
	- Export default
	- Import
	- How to use external libraries

- [EXERCISE] Create a component that displays the name of your favourite car and a picture of it and use it in `App`

- Creating HTML with JSX
	- JSX as a syntax extension to JS
	- JSX elements
	- HTML in JS file
	- JSX attributes
	- JSX outer elements

	- Writing regular JS in JSX
	  - Markers
	  - `<h1>{ 5 + 4 }</h1>`
	  - Scope in markers

	- Variable attributes
	- JSX conditionals
	  - Ternary not if's

- CSS in React
    - class vs className
    - [SASS in React](https://create-react-app.dev/docs/adding-a-sass-stylesheet/)

- Event listeners in React
	- Keyboard
	- Form
	- Focus
	- Mouse
	- [Useful events to know](https://reactarmory.com/guides/react-events-cheatsheet)

- Functions in components
```jsx
const Example = () => {
	const handleClick = (e) => {
		console.log('clicked')
	}
	
	return (
		<h1 onClick={handleClick}>Click me!</h1>
	)
}
export default Example
```

- [EXERCISE] Create a button component that console.logs how many times it has been clicked

- Props
	- Inside the component definition:```<p>This component was made by: { props.createdBy }</p>```
	- When you use your custom component:```<MyComponent createdBy="Charlie" />```
	- You can also destructure the props in the parameter: ```const Example = ({createdBy}) => { }```
	- You can pass any data type and functions
	- Handing data down the chain
	- [EXERCISE] Create a prop for the above button to pass in the text for that button

- State
	- A place to store data
	- Any change in data stored in state will trigger a rerender of that component and all its children
	```jsx
	import {useState} from 'react';

	const Example = () => {
		const [name, setName] = useState('Mike');

		return (<h1>Hello {name}</h1>)
	}
	```
	- Alter state with the setter function
	- Props and State can be used together:
	```jsx
	import {useState} from 'react';

	const Example = (props) => {
		const [name, setName] = useState(props.name);

		return (<h1>Hello {name}</h1>)
	}
	export default Example;
	```
	- [EXERCISE] Store the button click count in state and display it on the button after the prop text

- [Hooks](https://reactjs.org/docs/hooks-intro.html)
	- What are they and how are they used?
	- [State is a built in Hook](https://reactjs.org/docs/hooks-state.html)
	- [Effect Hook](https://reactjs.org/docs/hooks-effect.html)
	- Additional practice/reading: [Hooks Cheatsheet](https://react-hooks-cheatsheet.com/usestate)
	- Additional reading: [Custom hooks](https://reactjs.org/docs/hooks-custom.html)
	- [EXERCISE] Create a useEffect hook to console.log your name every 5 clicks
- Data flow in React

- Lifting State up

- [EXERCISE] Choose from below:
	- Build a component that tells you how many chocolate bars 1 bitcoin buys you (logic based on: https://codepen.io/charliecog/pen/WJyOVd)
	- Build a [tip splitting calculator](https://dev.io-academy.uk/resources/tip-splitter.jpg)
	- Build the challenge

- Additional reading:
	- [30 seconds to code - JS snippets](https://30secondsofcode.org/array)
	- [You Might Not Need JavaScript](http://youmightnotneedjs.com/)
	- [Modern javascript explained for dinosaurs](https://medium.com/@peterxjang/modern-javascript-explained-for-dinosaurs-f695e9747b70)
	- [State of JS](https://stateofjs.com/)
