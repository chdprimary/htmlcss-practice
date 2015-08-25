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
