### HTML / CSS Page Design Workflow

1 Create base HTML
```
	1a. DOCTYPE, html, head, meta utf-8, body
	
	1b. semantic structure
	
	1c. <a> links
	
	1d. text content
```	
2 Perform CSS layout
```
	2a. CSS reset
	
	2b. CSS clearfix
	
	2c. display, width, padding, border, margin, float additions
```	
3 Style content
```
	3a. color, font, font-sizes, line-heights
	
	3b. text-decoration, text-transform, text-align
```	
4 Style backgrounds

5 Style embedded media / forms

### CSS Layout - [learnlayout.com](learnlayout.com)
- ```display``` property
- block level elements take up full width of parent by default, unless you set ```width```
	- after setting width you can set ```margin: 0 auto``` to horizontally center the element inside its parent
	- if the browser window becomes smaller than the element, a horiz. scrollbar will appear
		- can fix by setting ```max-width``` instead of ```width```, which will resize element down on small screens
- ```box-sizing``` can be set to ```content-box``` (default), ```padding-box```, or ```border-box``` (which works padding, border, and margin inward instead of outward)
	- This is IE8+ only. Shouldn't use without plan B on sites where audience are accessing from work and/or are non-tech-saavy
- ```position``` can be ```static```(default), ```relative```(can use top,bottom,left,right), ```fixed```(fixed in viewport even when scrolling), or ```absolute```(positioned relative to nearest non-static ancestor)
- ```floats``` and ```clears``` and ```clearfixing```
- ```@media``` queries
	- e.g. ```@media screen and max-width:599px {```
- ```flexbox```

### Sass
- $var-name: var-val
- nesting
- @imports let you import "partials" (partial css files) to reduce number of HTTP requests (CSS file consolidation)

### Frontend Questions
- How many resources will a browser download from a given domain at a time?
	- IE7 and below: 2
	- IE8+: 6
	- Chrome: 6
	- Firefox: 8
- If you have 5 different stylesheets, how would you best integrate them into the site?
	- Possibly using Sass and @imports
- Name 3 ways to decrease page load (perceived or actual load time).
	- Minify everything
	- consolidate CSS/JS resources
	- use image sprites
	- gzip content (browsers understand gzipped content)
	- place ```<script>``` tags at bottom of ```<body>```
- How to avoid FOUC?
	- Put ```display: none``` on page elements until ```<script>``` near ```</body>``` executes, unhiding them.
- What does CORS stand for and what issue does it address?
	- Cross-Origin Resource Sharing, allows people to make restricted AJAX requests for resources on another domain. Partial solution to same-origin policy issue.
- What does a ```doctype``` do?
	- Tells the browser which standard to render the HTML as
- What's the difference between standards mode and quirks mode?
	- Browser modes. Standards mode renders according to standards. Quirks mode is used for old web pages and adds "intuitive functionality".
- What's the difference between HTML and XHTML?
	- XHTML is more strict, and less commonly used. Most contemporary sites use HTML5 by default (```<!DOCTYPE html>```)
- What are data-* attributes good for?
	- You can attach misc non-visual information to HTML tags, and easily access them from JavaScript. They tags may be named anything so long as they begin with "data-"
- Describe the difference between a cookie, sessionStorage and localStorage.
	- all are client-side storage
	- cookies are 4K old-school name-value pairs, sessionStorage is larger & tab-scoped, localStorage is also larger & domain-scoped.
- Describe the difference between ```<script>```, ```<script async>``` and ```<script defer>```.
	- Normal ```<script>``` will pause HTML parsing
	- async and defer begin downloading as soon as encountered, but don't pause the parser
	- defer scripts execute only after DOM is completely loaded, still execute in order specified in markup, even if the downloads complete out of order
	- async scripts execute as soon as finished, regardless of script specification order or whether DOM is finished loading or not
- What's the difference between "resetting" and "normalizing" CSS? 
	- Normalize.css iss more complex, doesn't unstyle everything (just "unuseful" default styles), and requires more attention
	- CSS reset is more "quick-and-dirty"
- What's the difference between inline and inline-block?
	- [answer](http://stackoverflow.com/questions/8969381/what-is-the-difference-between-display-inline-and-display-inline-block)
- Describe pseudo-elements and discuss what they are used for.
	- psuedo elements such as ```::before``` and ```::after``` can be used for many different things. They are both attached to each element on the page. They are inline by default. They allow you to add / manipulate styles before and/or after each element.
- What are some of the "gotchas" for writing efficient CSS?
	- avoid selectors that may match a large number of items (e.g. tag selectors) and minimize redundant selectors.
- 

### Great Resources
- [Learn HTML & CSS](http://learn.shayhowe.com/html-css/)
- [Learn CSS Layout](http://learnlayout.com/)
- [HTML Living Standard - WHATWG](https://html.spec.whatwg.org/multipage/semantics.html)
- [CSS Selectors Reference](http://www.w3schools.com/cssref/css_selectors.asp)
- [Website Performance Optimizations](http://www.sitepoint.com/web-site-optimization-steps/)

What excites or interests you about coding?
- data visualization project
