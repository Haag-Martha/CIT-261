## Code Topic Fluency 

### DOM
> Manipulation Using createElement, appendChild, insertBefore, removeChild, etc.

DOM stands for **D**ocument **O**bject **M**odel. It's a Model created in a structure similar to a tree. The top of this tree is the **document** object and all elements on the page inherit from it. The picture below demonstrate an example:

<img src="http://goliveira.com/byui/resources/html-tree.gif" />

The html source for this DOM tree structure is the following:

````html
<html>
<head>
  <title>My title</title>
</head>
<body>
  <a href="http://github.com">My link</a>
  <h1>My header</h1>
</body>
</html>	
````
The elements are added at the DOM even considering the moment when they were inserted on the page. On the node of the element `<body>`, the element `<a>` comes first on the node, before the `<h1>` element because that's how it was written on the source code.

The advantage of this tree structure is that we can add elements inside at any elements (nodes) after or before them,  and even creating new nodes to **parent nodes** (*any node that has a child is a parent node*).

In the example below, there is a demo of an TODO List App, where a list of items 'to be done' can be created. When the Button 'Add' is clicked, the function `addItem` is fired and them the `createElement` function is called to create a new `<LI>` element, them the property `innerText` of this element gets the value of the txtTodo input, also it assigns a function (`removeItem`) when the user click on this element.

The last step is to append this new `<LI>` element on the `<UL>` list with the `appendChild` function.


````html
<script>
  var myList = document.getElementById("myList");
  var txtTodo = document.getElementById("txtTodo");

  function removeItem(itemToRemove){  
    myList.removeChild(itemToRemove);
  }

  function addItem(){
    var newLiChild = document.createElement("li"); 
    newLiChild.innerText = txtTodo.value;
    newLiChild.onclick = function(){ removeItem(this); };
    myList.appendChild(newLiChild);

    txtTodo.value = "";
  }
</script>  
}
````

<a href="https://codepen.io/mintnerknown/pen/ExjxyGq" target="_blank">A complete source of this TODO App (At CodePen)</a>
