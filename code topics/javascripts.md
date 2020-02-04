## JavaScript Fluency
Version 2  Week 5
Feb 4, 2020

<a href="https://haag-martha.github.io/">Back to Home</a>



### JavaScript
Concepts: Loops, Conditional Statements, Functions, Variables, Parameters, Arrays, and Associative Arrays

All these examples occur within a scripts file (file extension .js) referenced within an HTML page structure. 

#### Variables
Variables are containers where data is stored. In the code below, the 'myOwnName' is a variable. The *var* before the variable designates it as a variable in JavaScript. The equal sign (=) is used to assign the value 'Martha Haag' to the variable.

```html
<script>
  //example of a variable
  var myOwnName = "Martha Haag";
  document.write(myOwnName); //display the value of the variable.
</script>
```
See it at 
<a href="https://codepen.io/mintnerknown/pen/vYEPJGY">CodePen</a>

#### Arrays
an array is a single variable that can store multiple elements. Multiple values are assigned within square brackets [ ].
For example:

```html
<script>
  //create a varialbe and assign values within the square brackets
  var Fruit = ["Apple","Banana","Coconut"];
  //display the first value of the array
  document.write(Fruit[0]); 
</script>
```
See it at 
<a href="https://codepen.io/mintnerknown/pen/dyPrzpx" target="_blank">CodePen</a>

#### Associative Arrays
In the example above, when accessing the first item (fruit) on the Array 'Fruits', with the [0] index, we are acessing something called *associative array*. We can only access arrays by their position in the Array. This is a zero based array, so the first item is in the position 0. and the last one is 2. (0 - Apple, 1 - Banana, 2 - Coconut). 

#### Functions and Parameters
A function is a block of code inside a { } curly brackets that execute a particular task. It needs to be inside a function declaration (or header) that it's composed by the *function* keyword, next to the name of the function and the ( ) parentheses. To pass parameters, we only need to name them inside the ( ) parentheses, separated by a comma when there is more then one. 

In the example below there a function (doTheMath) that multiplies two values passed to it through the parameters (param1 and param2). Those parameters are acessible only inside the scope of the function (outside the doTheMath function those values are to accessible).


```html
<script>
  //declare a function, name it, and create a math problem -in this case simple multiplication
  function aLittleMath(param1, param2){
    return param1 * param2;
  }
  //assign a variable for the result and assign values to the parameters
  
  var result = aLittleMath(40, 21); //this calls the function declared above passing the values 40 and 21 as parameters. This is very simple and will only work with integers as parameters
  
  document.write(result); //display the result.
</script>
```
See it at 
<a href="https://codepen.io/mintnerknown/pen/abzMyWX" target="_blank">CodePen</a>


#### Conditional Statements (If, Else)
Conditional statements execute specific blocks of code only if a condition is met.  In the following function 'aLittleMath,' it checks if the values are valid numbers.  If the values *are* valid (which comes up as false), the function will run.  In JavaScript "isNaN" is a built in function that checks if a value is NaN (not a number.) In the function *aLittleMath* the parameter values are validated as numbers before they are multiplied. 


```html
<script>
  //using the built in isNan function, validate the parameters as numbers
  function aLittleMath(param1, param2){
    if(isNaN(param1) == true) {
      return -1; 
    }
    else if (isNaN(param2) == true) {
      return -1;
    }
  
    //If param1 and param2 are valid numbers, then the function is executed and a value returned
    return param1 * param2;
  }
  
  var result = aLittleMath(40, 21);
  document.write(result);
</script>
```
See it at 
<a href="https://codepen.io/mintnerknown/pen/oNgVeqN" target="_blank">CodePen</a>


#### Loops (For and While)
Loops will continue excute a block of code over and over again as long as a specified condition is true. You can change the value the loop runs every time too. They *will* go on forever unless an end is specified.

In a simple for loop, a statement that will run a loop from 0 to 9 would be:

```html
<p id="loop"></p>
<script>
var text = "";
var i;
for (i = 0; i < 10; i++) {
  text += "number " + i + "<br>";
}
document.getElementById("loop").innerHTML = text;
</script>
```
See it at 
<a href="https://codepen.io/mintnerknown/pen/gObExBm" target="_blank">CodePen</a>


#### Demo Application

Here is a link to a simple test using many of the methods I talked about here.

<a href="https://codepen.io/mintnerknown/pen/VwYRzqe" target="_blank">A simple quiz</a> at CodePen
