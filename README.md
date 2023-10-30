# My journey learning code 🧐
## resources
1. [p5*Js creative code](https://p5js.org/)
2. [The nature of code on p5*Js follow along videos](https://www.youtube.com/watch?v=70MQ-FugwbI&list=PLRqwX-V7Uu6ZV4yEcW3uDwOgGXKUUsPOM)
4. [Nature of Code document](https://natureofcode.com/)
5. [processing](https://processing.org/)
6. [Code as a creative medium book](https://mitpress.mit.edu/9780262542043/code-as-creative-medium/)
7. [How to complete the books tasks](https://github.com/CodeAsCreativeMedium/exercises)
8. [Free books and documents](https://annas-archive.org/)
9. [Java Script for beginners](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
## What is JavaScript? 
JavaScript is used to add graphics or interactive pieces to your website, compared to HTML, which is used to create the foundations of a website. For example, JavaScript can edit  pieces of text (known as "strings" in programming). For example, we take the string "Player 1: " and join it to the name variable to create the complete text label, e.g. "Player 1: Chris". JavaScript can also be used to run code in response to certain events occurring on a web page. 
## p5*Js experiments
### Elipse
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(50,50,80,80);
}```
[]
### Green box and text following cursor
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
function setup() {
  createCanvas(400, 400);
 
}

function draw() {
   let inside = color(2, 200, 89)
   let p = createP('hi Im mollie and im trying really hard to code');
  p.style('font-size', '12px');
p.style('width', '65px');
p.style('text-align', 'center');
p.position(mouseX, mouseY, 100);
  if (mouseIsPressed) {
 fill(0);
  }else{
    fill(inside);
}
createP(mouseX, mouseY, 100) 
  square(mouseX, mouseY, 100)
}
```
[example](https://molliessss.github.io)
### 3D box with point light and web cam textures
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
// draw a spinning box
// with width, height and depth of 50
 // this variable will hold our webcam video
 let cam;
function setup() {
  createCanvas(1500, 1500, WEBGL);
  cam = createCapture(VIDEO);
   cam.size(710, 400);
  describe('a box rotating in 3D space with specular highlight. Clicking the mouse toggles the specular highlight color between rgb(255,255,255) and the default rgb(255,255,255).');
}

function draw() {
   background(0);
  // move your mouse to change light position
  let locX = mouseX - width / 2;
  let locY = mouseY - height / 2;
  // to set the light position,
  // think of the world's coordinate as:
  // -width/2,-height/2 ----------- width/2,-height/2
  //                   |           |
  //                   |    0,0    |
  //                   |           |
  //  -width/2,height/2 ----------- width/2,height/2
  pointLight(250, 250, 250, locX, locY, 50);
  texture(cam);
  rotateX(0.5);
  noStroke();
  sphere(200);
  background(200);
  rotateX(frameCount * 0.008);
  rotateY(frameCount * 0.008);
  box(mouseX, mouseY, 100);
}
```
[example](https://molliessss.github.io/3D/)
