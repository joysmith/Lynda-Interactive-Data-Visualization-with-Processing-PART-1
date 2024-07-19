1. [Using embedded data](#1)
2. [Working with appended text data](#2)
3. [Working with appended tabular data](#3)
4. [Reading XML data](#4)

---

### 1 App: Using embedded data<a id="1"></a>

<img src="assets/images/1.png" width="700">

```js
// Ex10_01

color[] dessert = {#9F9694, #791F33, #BA3D49, #F1E6D4, #E2E1DC};
color[] palette = dessert;

size(600, 200);
background(palette[0]);
smooth();

int[] fibonacci = {0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377};
for(int i = 0; i < fibonacci.length; i++){
//  noStroke();
//  fill(palette[2], 50);
  stroke(palette[1]);
//  strokeWeight(2);
  float x = fibonacci[i];
//  ellipse(x, height/2, 20, 20);
  line(x, 75, x, 125);
}
```

- ellipse() function reference documentation [click me]()

### 2 App: Working with appended text data<a id="2"></a>

<img src="assets/images/1.png" width="700">

```js
// Ex10_02

color[] crowds = {#678C8B, #8FA89B, #A2BAB0, #D0EDDE, #B3B597};
color[] palette = crowds;

void setup(){
size(600, 200);
//println(presidents);
PFont font;
font = loadFont("Aharoni-Bold-48.vlw");
textFont(font);
}

void draw(){
background(palette[0]);
fill(palette[2]);
String[] presidents = loadStrings("presidents.txt");
text(presidents[40], mouseX, mouseY);
}
```

- ellipse() function reference documentation [click me]()

### 3 App: Working with appended tabular data<a id="3"></a>

<img src="assets/images/1.png" width="700">

```js

```

- ellipse() function reference documentation [click me]()

### 4 App: Reading XML data<a id="4"></a>

<img src="assets/images/1.png" width="700">

```js
// Ex10_04

import proxml.*;

XMLInOut xmlInOut;

void setup(){
  size(600, 200);
  xmlInOut = new XMLInOut(this);
  xmlInOut.loadElement("http://api.wefeelfine.org:8080/ShowFeelings?display=xml&returnfields=feeling,postdate,sentence&limit=50");
}

void xmlEvent(proxml.XMLElement element){
  for(int i = 0; i < element.countChildren(); i++) {
    println(element.getChild(i).getAttribute("postdate"));
    println("\t"+element.getChild(i).getAttribute("sentence"));
  }
}
```

- ellipse() function reference documentation [click me]()
