

## p5.js
**p5.js** is a javascript library to make coding accessible for artists, designers, educators and beginners.

### p5.js Tutorial
  This tutorial is an attempt to give a quick inroduction to **p5.js** and consists of **short code** snippets with explanations in the comments section of the code.

  The Tutorial assumes you have installed or have access to the necessary p5.js files. Visit [p5.js](https://p5js.org/) in case you need installation details.

  if you do not want to install p5.js but want to quickly try things our then here is an [online editor/previewer](http://alpha.editor.p5js.org/).

  Have fun....

#### Program Structure
```javascript
  var x=0  // global variables

  function setup () {
    // runs once during the lifetime of this script
  }

  function draw () {
    // called 60 time every second by default

  }
```

Try this

```javascript
var bg=0  // global variables
var inc=1 // increment
function setup () {
  // create a canvas 400 pixels by 400 pixels
  createCanvas(400,400)
}

// called 60 time every second by default
function draw () {
  background(bg) // draw a background with grey shade indicated by bg
  bg = bg+inc    // increment bg by 1 every 1/60 of a second

  // ensure bg value oscillates between 0 and 255
  if (bg > 255) {
		inc = -1
		bg=255
	}

	if (bg < 0) {
		inc=1
		bg=0
	}
}
```
what you will notice is the that the **background** color of the **canvas** goes from white to black and black to white indefintely

#### Canvas

The *canvas* is where the `draw()` draws and is created by `createCanvas(w,h,[renderer])` function the renderer by default is *P2D*, other options being *WEBGL* in case you are interested is drawing 3d shapes. Read more about the [WEBGL here]( https://github.com/processing/p5.js/wiki/Getting-started-with-WebGL-in-p5)

Top left corner in the Canvas is `(0,0)` x-Axis runs from 0 on the left to positive numbers on the right, whereas the y-Axis starts with 0 on the top with positive numbers along y-Axis going down.

**need a small diagram here**

#### Lines

Drawing lines is simple. All you need is two points
 `(a,b)` and `(c,d)`. Using `line(a,b,c,d)` we will get a line connecting the two point.
```javascript
function setup() {
  createCanvas(400,400)
}

function draw() {
  line(x,10,100,150)
}
```
#### Shapes

One can also draw common shapes like ellipse, rectangle, triangle etc. see [p5 Reference](https://p5js.org/reference/) for more shapes

here is an example:

```javascript
function setup() {
  createCanvas(400,400)
}

function draw() {
  line(10,10,100,150)

  // given top left corner and width and height
  // draw a rectangle
  rect(10,10,100,100)

  // given a center point and width and height of
  // horizontal and vertical axis - draw a ellipse
  // if widht=height you get a circle

  ellipse(20,20,10,100)
  ellipse(10,100,50,50)
}
```


#### Mouse

Its possible to use mouse events and position to manipulate the graphics. `mouseX` and `mouseY` always refer to current mouse position.

The `mousePressed()` is called when mouse is pressed and the code here  will modify the position of ellipse being drawn.

```javascript
// let cx,cy be the position of center of ellipse
var cx=100
var cy=100
function setup() {
  createCanvas(400,400)
}

function draw() {

  // draw background of white every time draw is called
  // by doing this you will see only one ellipse
  // try running this script without background(255)
  background(255)
  // given a center point and width and height of
  // horizontal and vertical axis - draw a ellipse
  // if widht=height you get a circle

  ellipse(cx,cy,mouseX,mouseY)
}

// when mouse is pressed update center co-ordinates
function mousePressed() {
  cx = mouseX
  cy = mouseY
}
```
#### Sound

### Projects

#### 1. eyes
#### 2. Motion
#### 3. Music and Motion
#### 4. Generate Surface
