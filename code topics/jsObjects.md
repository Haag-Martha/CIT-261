## JavaScript Objects Fluency 

### JavaScript Objects
Concepts: Object Creation, Functions, Inheritance, Properties, Methods, Instantiation.

Object oriented programming: (OOP) This means that you use objects which contain data in programming.  One huge advantage is you can create modules that don't need to be changed when a new type of object is added.  I can just create a new object that inherits features from other existing objects.  Ulitately, this saves time and allows me to organize my program into bite size pieces which are much easier for my mind to process. 

JavaScript is not actually an object oriented language, but it 
uses objects and assigns properties and values to them.  It gets a little involved.  Objects are variables but may contain many values.  Basically, "JavaScript objects are containers for *named values* called properties or methods" <a href="https://www.w3schools.com/js/js_objects.asp">(w3schools.com)</a>


I my little snippet of code here, I create a class "rectangle" with a constructor (constructor: type of function executed on the creation of the object) with width and height properties in parenthesis ( ). Then I create two functions "calcArea" and "displayArea." Finally, I create a variable "rect_1" that is a rectangle object!  This variable is creating and "instance" of the rectangle class, an object.  All the data within the class (constructor, the two functions) are accessed by the object variable.


```html
<script>
  class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

    calcArea(){
      return rec1.width * rec1.height;
    }
    

   displayArea(){
          document.write(rec1.width + " x " + rec1.height + " = " + this.calcArea());
   }
    

}
  
  var rect_1 = new Rectangle(100, 200);
 rec1.displayArea();
</script>
```

See it work at <a href="https://codepen.io/mintnerknown/pen/gObEKee" target="_blank">CodePen</a>

Now, I understand this is rudimentary.  There is much more to learn and I can delve **deep** into the abyss of JavaScript Objects. But I have been given half of one week (3 days) to learn this.  I understand this in principle but need more time to really learn it.
