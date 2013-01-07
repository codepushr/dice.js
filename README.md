Dice.js
=======================================

A lightweight JavaScript library for random animated dice or simple calculated dice results.<br />
<a href="http://skripted.github.com/dice.js/demo/" target="_blank">Check out the Demo</a> (when animating).

Basic Usage
---------------------------------------

Include the main JavaScript file in the bottom of your HTML document:
```html
<script type="text/javascript" src="dice.min.js"></script>
```
Create a variable to hold the result and call the Object's init() method:
```html
<script type="text/javascript">
                 
    // param1: number to divide among multiple dice
    // param2: number to be ignored (in the random generator)
    var result = Dice.init(15, 10);
  
</script>
```    
You can even define optional arguments to override some default values:
```html
<script type="text/javascript">

	var result = Dice.init(14, 1, {
		animate : true,
		debug : true, 
		diceFaces : 6,
		diceSize: 200,	// px
		diceCls : { 	// class names
			box : 'diceBox', 
			cube : 'diceCube',
			face : 'face',
			side : 'side'
		},
		wrapper : 'diceHolder',
		xRange : [8, 16],  // min and max turns in x axis
		yRange : [8, 16],  // min and max turns in y axis
	});
  
</script>
```
When animating be sure to add the following rules to your CSS stylesheet:
```css
.diceBox {
  float: left;
  border: 1px solid red;
}

.diceCube {
  position: relative;
  -webkit-transition: -webkit-transform 2s ease-out;
  -webkit-transform-style: preserve-3d;

  -moz-transition: -moz-transform 2s ease-out;
  -moz-transform-style: preserve-3d;
}

.face {
  position: absolute;
  background-color: rgba(50, 50, 50, 0.9);
  border: 1px solid #555;
  border-radius: 3px;
}   
```
Also don't forget the rules for all sides of the cube (optionally with images):
```css
/* one of six ... */
.side1  {
  background-image: url(../img/face1.svg);
  -webkit-background-size: 100% 100%;
  -moz-background-size: 100% 100%;
}
```
Roadmap
---------------------------------------

There's still things to do. Currently it is possible to give more than 6 faces for the dice - 
but they will only affect the calculation when not animating. 
It does not yet affect the animation (which is 6 faces static at the moment)!

License Information
---------------------------------------
Copyright 2013 - by Aleksandar Palic - http://www.twitter.com/_skripted


Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
