# Module 1 - HTML & CSS

## Objectives

- Basic understanding of how the web works
- Understand and write HTML
- Understand what CSS is
- Ability to style HTML using CSS
- Understanding of the DOM and document Flow

## Challenge

- Build the HTML logo using HTML and CSS only (no images)
	- Due at first sprint review
	- Use [this font](https://cdn.rawgit.com/mfd/f3d96ec7f0e8f034cc22ea73b3797b59/raw/856f1dbb8d807aabceb80b6d4f94b464df461b3e/gotham.css) 
	- Do the CSS Logo too as a bonus
	<img src="https://dev.io-academy.uk/resources/logo/CSS-HTML-logo2.png" width="250">

## Programme

- Introduction to HTML
	- [What is HTML?](http://www.w3schools.com/html/html_intro.asp)
	- Syntax
	- Wireframing ([Examples](https://mockflow.com/samples/))
		- demo wireframing a website live
		- [EXERCISE] - pick a website and wireframe a page 
	- [Document flow](http://webdesign.tutsplus.com/articles/quick-tip-utilizing-normal-document-flow--webdesign-8199)
 
- Understanding different Tag types (div vs section)
	- [HTML Tags](http://www.w3schools.com/tags/)
		- Useful tags: `<a>, <div>, <h1> to <h6>, <img>, <ul>/<ol> with <li>, <section>, <strong>` 
	- [W3 Spec](http://www.w3.org/TR/html/)
	- [Forms](https://www.w3schools.com/html/html_forms.asp)
	- Tables
	- [HTML validator](https://validator.w3.org/#validate_by_input)
	- [EXERCISE] -  using only valid HTML build a page with a heading(h1) containing your name, under that create an email address input field, a link to google.com, an image and a bullet pointed list of your favourite foods.  

- Introduction to the web
	- Http requests
	- DNS
		- [Additional Reading](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts)
	- Browser Parsing
	- [Additional Reading](http://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)

- Introduction to CSS 
	- Basic syntax
	- Inline styles vs head styles vs CSS file
	- [Additional Reading](http://www.cssbasics.com/introduction-to-css/)

- CSS Properties
	- [All Properties](http://www.w3schools.com/cssref/default.asp)
	- [CSS Colours](http://www.w3schools.com/cssref/css_colors.asp)
	- [CSS Units](http://www.w3schools.com/cssref/css_units.asp)
	- [EXERCISE] - Link an external css file to your build and change background colour + text colour

- Understanding CSS styling
	- UI and UX ref: Uber
	- [CSS Tricks](https://css-tricks.com/)
	
- Using selectors
	- Class & ID
		- Semantics & naming conventions
	- Other selectors
		- [Pseudo selectors](http://www.w3schools.com/css/css_pseudo_classes.asp)

- CSS Concepts
	- [Display types](http://www.w3schools.com/css/css_display_visibility.asp)
		- Block
		- Inline
		- None
		- ref: Document flow
	- [Floating](http://www.w3schools.com/css/css_float.asp)
		- [EXERCISE] - Use float to place the image and the bullet pointed list next to each other
	- [Inline-Block](https://www.w3schools.com/css/css_inline-block.asp)
	- [Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
		- Use this for components, not for layout
		- [How different flexbox properties work](https://medium.freecodecamp.org/even-more-about-how-flexbox-works-explained-in-big-colorful-animated-gifs-a5a74812b053)
		- Additional Reading/Fun: [Flexbox Froggy](https://flexboxfroggy.com/)
	- [Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
		- Use this for layout, not components
		- [Columns](https://www.w3schools.com/cssref/pr_grid-template-columns.asp)
		- [Rows](https://www.w3schools.com/cssref/pr_grid-template-rows.asp)
		- Additional Reading/Fun: [CSS Grid Garden](https://cssgridgarden.com/)
		
	- [CSS Box Model](http://www.w3schools.com/css/css_boxmodel.asp)
		- Always change the default box model
		- Default margin/padding on body
	- CSS resets [Normalize](https://necolas.github.io/normalize.css/)

- [Exercise]: [Build this](https://dev.io-academy.uk/resources/jumbotron-desktop.png) (does not have to be responsive)

	- [Positioning](http://www.w3schools.com/css/css_positioning.asp)
		- Static
		- Relative
		- Absolute
		- Fixed

- Working as a team
	- Pair programming
		- [Additional Reading](https://tuple.app/pair-programming-guide/)
		- [EXERCISE] [Build this form](https://htmlpreview.github.io/?https://github.com/iO-Academy/twbs-form/blob/master/index.html)
			- Don't worry about validation!
	- [Rubber ducking](https://rubberduckdebugging.com/)
	- [Code Review](https://dev.to/mporam/good-code-reviews-43kk)
		- [What to review](https://github.com/iO-Academy/FST-curriculum/blob/master/code-reviews.md)
		- [EXERCISE] Swap previous exercise code with another group and code review
	- Building an online presence
		- Github, dev.to, stackoverflow, blog, twitter, meetups/joind.in

- Debugging and cross browser issues
	- Browsers and Evergreen
	- Browser/Vendor prefixing
		- https://autoprefixer.github.io/
	- Inspector
 	- [caniuse.com](http://caniuse.com/)
		- [Example](https://caniuse.com/#feat=mdn-css_properties_aspect-ratio)
	- Browser testing
		- [BrowserStack](https://www.browserstack.com/)
		- [EXERCISE] Sign up to github [student developer pack](https://education.github.com/pack/offers#browserstack)

- Introduction to the DOM
	-  [What is the DOM?](https://css-tricks.com/dom/)
	
- Responsive Development
	- Graceful degradation (new first) vs progressive enhancment (old first)
	- % units
	- [Media Queries](https://www.w3schools.com/cssref/css3_pr_mediaquery.asp)
		- Mobile first vs Desktop first
	- Meta tag scaling [responsive meta tag](https://css-tricks.com/snippets/html/responsive-meta-tag/) 
	- ems vs rems [font sizing with REMs](https://snook.ca/archives/html_and_css/font-size-with-rem)

- [EXERCISE] Update your jumbotron build to be [responsive for mobile](https://dev.io-academy.uk/resources/jumbotron-mobile.png)

- Command Line
	- [Common commands](http://www.computerworld.com/article/2598082/linux/linux-linux-command-line-cheat-sheet.html)
	- Setting up your PATH
		- Use [OhMyZsh](https://github.com/ohmyzsh/ohmyzsh)
		- [EXERCISE] [Pick a theme](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) and configure it
	- Alias'

- Git - [Cheatsheet](http://rogerdudler.github.io/git-guide/)
	- What is it?
	- Setting up Git
		- [Download it](https://git-scm.com/download/mac)
		- Configure [username](https://help.github.com/articles/setting-your-username-in-git/) & [email](https://help.github.com/articles/setting-your-commit-email-address-in-git)
		- Configure text editor
			`git config --global core.editor nano`
		- [Connect to Github](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
	- Branching
		- [Additional Practice](https://learngitbranching.js.org/)
	- Cherry picking
	- Reverting
	- Merge conflicts
	- Merge tools (Pull requests)
	- [EXERCISE](https://github.com/iO-Academy/git-workshop) Create a pull request to test repo
 	- [UIs](https://desktop.github.com/) 
	- Git log
	- [.gitignore](https://www.freecodecamp.org/news/gitignore-what-is-it-and-how-to-add-to-repo/)
		- [Tool for creating one for you](https://www.toptal.com/developers/gitignore)
		- [Suggested config](https://www.toptal.com/developers/gitignore/api/osx,phpstorm,phpunit,react)

- [EXERCISE] [Build this page](https://pilot-shop-equipment.myshopify.com/)

Additional Reading:
- [snippets of useful media queries](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)
- [Google for colours](https://picular.co/)
- [Want more practise?](https://www.frontendmentor.io/challenges)
