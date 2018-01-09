# Project documentation

This site documents most project in my [GitHub repository](https://github.com/ugmurthy)

## DeepLearning


## p5.js examples

### Tutorial
  This Tutorial on p5.js will be based on **short code** snippets with explanations in the comments section of the code.
  The basic idea is to get you started quickly. The Tutorial assumes you have installed or have access to the necessary p5.js files. Visit [p5.js](https://p5js.org/) for details

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

Lets draw a line connecting two points `(a,b)` and `(c,d)` - `line(a,b,c,d)`
```javascript
function setup() {
  createCanvas(400,400)
}

function draw() {
  line(10,10,100,150)
}
```
#### Shapes
#### Mouse
#### Sound

### Projects

#### 1. eyes
#### 2. Motion
#### 3. Music and Motion
#### 4. Generate Surface
