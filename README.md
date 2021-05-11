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
### Render tree construction

While the Dom tree is being constructed, the browser constructs another tree called __Render tree__.
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
### Resource 
* [Browser Rendering video lecture.](https://www.youtube.com/watch?v=SmE4OwHztCc&t=1477s)
* [How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/#Introduction)
