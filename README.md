Dice.js
=======================================

A lightweight JavaScript library for random animated dice or simple calculated dice results.

Basic Usage
---------------------------------------

Include the main JavaScript file in the bottom of your HTML document:

    <script type="text/javascript" src="dice.js"></script>

Create some return variable and call the Dice Object's init() method:

    <script type="text/javascript">
    
      window.onload = function() {                     
      
        var result = Dice.init(15, 10);
      	console.log(result);
      
      };
      
    </script>
    
You can even define optional arguments to override some default values:

    <script type="text/javascript">
    
      window.onload = function() {                     
      
        var result = Dice.init(15, 10, { 
      		animate : true, // if animating
    			debug : true, // to debug to console
    			diceFaces : 6, // dice face number
    			parent : 'diceHolder', // id of the parent
    			xRange : [8, 16], // x turns min and max
    			yRange : [8, 16], // y turns min and max
    			cssProp : 'WebkitTransform' // translate property
    		});
        
        console.log(result);
      
      };
      
    </script>

When animating be sure to add the following rules to your CSS file:

    .diceBox {
      -webkit-perspective: 600; 
      -webkit-perspective-origin: 50% 200px;
      -moz-perspective: 600; 
      -moz-perspective-origin: 50% 200px;

      float: left;
      border: 1px solid red;
      width: 400px;
      height: 400px;
    }

    .diceCube {
      position: relative;
      margin: 100px auto;
      height: 200px;
      width: 200px;
      -webkit-transition: -webkit-transform 2s ease-out;
      -webkit-transform-style: preserve-3d;
    
      -moz-transition: -moz-transform 2s ease-out;
      -moz-transform-style: preserve-3d;
    }
    
    .face {
      position: absolute;
      height: 200px;
      width: 200px;
      background-color: rgba(50, 50, 50, 0.9);
      font-size: 27px;
      line-height: 1em;
      color: #fff;
      border: 1px solid #555;
      border-radius: 3px;
    } 


