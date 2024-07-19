1. [Interacting with zooming, rotating, and sliding](#1)
2. [Implementing slicing](#2)
3. [Using rollovers](#3)
4. [Introducing the GUI libraries](#4)

---

### 1. Interacting with zooming, rotating, and sliding<a id="1"></a>

<img src="assets/images/1.png" width="700">

```js
// Ex13_01

int d = 40;

float xo;
float yo;
float zoom = 1;
float angle = 0;

void setup() {
  size(600, 200);
  xo = width/2;
  yo = height/2;
  smooth();
  noStroke();
}

void draw() {
  background(#1F7B9B);
  translate(xo, yo);
  scale(zoom);
  rotate(angle);

  fill(120);
  ellipse(-200, 0, d, d);
  fill(180);
  ellipse(-100, 0, d, d);
  fill(220);
  ellipse(   0, 0, d, d);
  fill(180);
  ellipse( 100, 0, d, d);
  fill(120);
  ellipse( 200, 0, d, d);
}

void keyPressed() {
  if (key == CODED) {
    if (keyCode == UP) {
      zoom += .03;
    } else if (keyCode == DOWN) {
      zoom -= .03;
    } else if (keyCode == RIGHT) {
      angle += .03;
    } else if (keyCode == LEFT) {
      angle -= .03;
    }
  }
  if (key == ' ') {
    angle = 0;
    zoom = 1;
    xo = width/2;
    yo = height/2;
  }
}

void mouseDragged() {
  xo = xo + (mouseX - pmouseX);
  yo = yo + (mouseY - pmouseY);
}
```

- ellipse() function reference documentation [click me]()

### 2. Implementing slicing<a id="2"></a>

<img src="assets/images/1.png" width="700">

```js

```

- ellipse() function reference documentation [click me]()

### 3. Using rollovers<a id="3"></a>

<img src="assets/images/1.png" width="700">

```js

```

- ellipse() function reference documentation [click me]()

### 4. Introducing the GUI libraries<a id="4"></a>

<img src="assets/images/1.png" width="700">

```js

```

- ellipse() function reference documentation [click me]()
