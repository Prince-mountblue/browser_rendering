# Browser Rendering
### what is a web browser?

A web browser is a piece of software that loads a file from a remote location and renders it on your screen.
![Rendering image ](https://miro.medium.com/max/4848/1*uY2K9BXnJ-uP4X9vAPvfDg.png)Example of web browser are Internet Explorer , Google Chrome, Mozilla Firefox, Safari, Opera and others.
### The browser's high level structure 
![Browser high level structue](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/layers.png)

### Browser engine
A browser engine is the core software of every web browser. The primary job of the browser engine is to convert resource into an interactive visual accept on the user machine.

###  Rendering engine 
Responsible for displaying requested content. Content Like (HTML, CSS) 
![Browser engine](https://sreejithav.files.wordpress.com/2013/05/bengines.png)
### High-level Flow of browser rendering
![Main flow](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/flow.png)
###  Parsing HTML to construct the DOM tree
* __Parsing__: is used to derive a string using the production rules of a grammar. 
* __Parsing HTML__:  The rendiring engine will start parsing the HTML document and convert elements to DOM node of tree called content tree. 
![DOM nodes](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/image015.png)

#### Document object Model (Dom)
When the browser reads HTML code, it creates a JavaScript object calle a __Node__.
* All the elements will be coverted to JavaScript Objects.
* After the browser has created _Nodes_ from the HTML document, it has to create a __tree-like structure__ of these node objects.
![Dom tree in details](https://miro.medium.com/max/1040/1*YSA8lCfCVPn3d6GWAVokrA.png)
We can visualize the DOM tree in Google Chrome DevTools
![Chrome](https://miro.medium.com/max/700/1*Uo2wfq060OMSLyTTCm2zFw.png)
 #### CSS Object Model (CSSOM)
 After constructing the DOM, the browser reads CSS from all the souces (external, inline etc) and construct a CSSOM.
 * It is a tree like structure just like dome.
 * CSSOM does not contain DOM elements which can't printed on the screen like 
 ``` <meta> , <scripts>, <title> etc. ```
 ![CSSOM Tree](https://miro.medium.com/max/357/1*DJg1yRx-AzkZposWbJKcaA.png)
### Render tree construction

It is also a tree-like structure constructed by combining DOM and CSSOM tree together , the browser constructs this tree called __Render tree__.
* This tree is of visual elements in the __order__ in which they will be displayed.
* It is the _visual representation_ of the document.
* The purpose of this tree is to enable painting the contents in their correct order.
 
![Render tree with dom tree](https://miro.medium.com/max/7602/1*8HnhiojSoPaJAWkruPhDwA.png)
### Layout 
When the renderer is created and added to the tree, it does not have a position and size. Calculating these values is called layout or reflow.
Layout is a recursive process. It begins at the root renderer.

### Paint operation 
In the painting stage, the render tree is traversed and the rendere's __paint()__ method is called to display content on the screen. 
Painting uses the UI infrastructure components.
### Resources & links 
* [Browser Rendering video lecture.](https://www.youtube.com/watch?v=SmE4OwHztCc&t=1477s)
* [How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/#Introduction)
* [DOM and CSSOM with code example](https://medium.com/jspoint/how-the-browser-renders-a-web-page-dom-cssom-and-rendering-df10531c9969)
