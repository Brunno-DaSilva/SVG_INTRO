# SVG_INTRO

The lecture is about SVGs

1. We are going to learn what SVGs are
2. Learn to Draw SVGs with a text editor
3. Understand the basic properties and behaviors of SVG

You would normally use a design tools to drawn SVGs, however,  
It is really important to understand what the code means to effective work with it.

---

### Intro:

There are two major systems for representing graphic information on computers:

**Raster Graphics**: Images are represented as rectangular arrays of pixels.

Some examples are: "JPEG, GIFs PNGs"

    Pros: Complex images

    Cons: They are Difficult to scale up and down

**Vector Graphics**: Images are represented as geometric shapes.

    Pros: Can scale up and down - without loss of image quality

    Cons: Difficult to make ultra complex images

    Examples of less complex shapes:

Logos
Minimal graphics ( Social Media icons, buttons, arrows)

### More About SVGs:

- SVGs are scalable without loss of quality

- SVGs are Part of the HTML standards since late 90s

- SVGs are written with XML tags and have attributes

- Thus, it can be manipulated by CSS and JavaScript making it even more dynamic.

#### Take a look at these examples:

SVG icons: `https://www.flaticon.com/home`

SVG Animation sites:

`https://www.thewwwmagazine.com/6-amazing-svg-animation-tools-and-libraries/ More SVG Examples: https://bashooka.com/coding/30-mindblowing-examples-of-svg-animation/`

---

### Getting Start:

Check out some SVGs in an HTML page

- Open the `svg-example.html` file
- Open Chrome Developer Tools
- Inside the `div` with the class `container` are two SVGs

  - The first one is a pie chart that is created with D3 (library like jQuery)
  - The second one is the legend for the pie chart created in Sketch.

- This is a lot of complex code! We're going to build our very own modern art project that is going to deconstruct some of the basic components of SVGs so that we can understand them and be able to use them effectively

**Bonus**: Excellent read on learning D3/Learning how to code anything.
How do you learn d3.js?

`https://medium.com/@enjalot/how-do-you-learn-d3-js-ccffc151419b`

### SVG Basics

There are some common shapes for:

- Rectangle
- Circle
- Line
- Text
- Ellipse \*
- Path - more complicated shapes - like triangles or outlines of countries/states \*
  \* We will not cover these today
  We're going to learn about SVG and these shapes, but using an investigational approach.

- Go ahead and open modern-art.html

**Note**:

    `<g> = Group`

<details><summary>Final Outcome</summary>

## ![modern art](https://i.imgur.com/NMmUYLZ.png)

### SVG:

1. The first thing to do is to add an svg element. Below the <h1> tag - Add

`<svg></svg>`

2. Open modern-art.html in your web browser

`Where is the svg? Open Chrome Developer tools ⌘ ⌥ I`

It is there, but it is not visible. Make it visible by adding the `attribute` of a border

When styling SVG we use attribute:

`<svg style="border:1px solid blanchedalmond;"></svg>`

`Remember: SVGs are based on web standards, so we can use html attributes, including inline-style CSS.`

    3. Let's set a height and width of 500 pixels. Height and width are two attributes of SVGs (you could also set this with CSS, but the convention is to set them as attributes)

    <svg style="border:1px solid blanchedalmond" height="500px width="500px">
    </svg>


    4. It is important to also think of the SVG as having a coordinate system, like a graph.

    	For example (using the first coordinate as the x and the second as y):

    	○ position 0 , 0 is the upper left corner
    	○ position 0 , 500 is the bottom left corner
    	○ position 500, 0 is the upper right corner
    	○ position 500, 500 is the bottom

    5. Notice, that if you don't include units it will default to pixels, but you can use em or other responsive unity.

    	<svg style="border:1px solid blanchedalmond" height="500px" width="500">
    	</svg>


    6. We can add more CSS attributes, let's move the element over so it isn't right up against the left side of the browser:

    	<svg style="border:1px solid blanchedalmond; margin-left:100px;" height="500px" width="500"></svg>

---

### RECTANGLES:

    1. Inside the SVG element add

    <rect />

    2. Without Attributes  you can really see it, so lets add some properties

    Let's give it a width and height:

    	<rect width="200" height="200"/>

Important: Before we jump into the next part. It is important to take note of the default behaviors of this shape

    	○ Write in slack - Where did the rectangle go?

    	○ Write in slack - What color is the rectangle?

    3. Let's go ahead and change the color of the rectangle. In order to do that, we have to use an attribute called fill=""

    	We can use names, hexadecimal, rgb, rgba, hsl...

    	 <rect height="200" width="200" fill="hotpink" />


    4. Add another Rectangle Above our first rectangle

    	<rect height="200" width="200" fill="gold" />
    	<rect height="200" width="200" fill="hotpink" />

    	○ Write in slack what happened?


    5. Let's move our gold rectangle over a bit, by adding x and y coordinates

     <rect height="200" width="200" fill="gold" x="100" y="100"/>

    6. Let's swap the order or our gold and hot pink rectangles

    	 <rect height="200" width="200" fill="hotpink"/>
    	 <rect height="200" width="200" fill="gold" x="100" y="100"/>

    7. Let's add a Third Rectangle drop your code into slack
    	a. Fill - slightsalmon
    	b. W and H - 200
    	c. Give negative coordinates -100 for x and y
    	d. Put it after the gold rectangle.


    8. Let's talk about what happened

    	○ Can we have negative coordinates?

    	○ Where will the rectangle go?

    	○ Give the code to the class

    9. Another property of rectangles is the border in SVG it is called Stroke

    <rect height="200" width="200" fill="gold" x="100" y="100" stroke="darkorange"/>


    10. Stroke defaults to 1px, but we can change by adding another property called Stroke-Width

    <rect height="200" width="200" fill="gold" x="100" y="100" stroke="darkorange" stroke-width="50" />

    11. Let's add some transparence
    	a. You can add it by using the opacity attribute
    	b. Which properties range from 0-1
    	c. Note: you can also add transparence using rgba() colors or hsla() colors
    	d. Note: When using opacity="" it applies to the entire element

    <rect height="200" width="200" fill="gold" x="100" y="100" stroke="darkorange" stroke-width="50"opacity=".9" />

    <rect height="200" width="200" fill="hotpink" x="100" y="100" stroke="darkorange" stroke-width="50"opacity=".5" />

    12. Just like CSS, you can rotate, skew, translate etc. SVG elements.

    <rect height="200" width="200" fill="gold" x="100" y="100" stroke="darkorange" stroke-width="50"opacity=".9" transform="rotate(45, 175 , 275)" />

### What we are missing from our final goal?

<details><summary>Final Outcome</summary>

## ![modern art](https://i.imgur.com/NMmUYLZ.png)

### Lines:

    1. Let's add two lines on top of our rectangles

    	○ Does that mean the line elements should go before or after the rectangles? After

    	a. Lines require a start and end point, therefore, they need 4 coordinates
    	b. The starting coordinates are x1="" y1=""
    	c. The end coordinates are x2="" y2=""
    	d. So to draw a line from the upper left corner, down to the bottom left we would do:

`<line x1="0" y1="0" x2="500" y2="500" />`

```
Important: If you add this code you should not see anything, because unlike rectangles, lines have no default color.
```

`i. Lines are made of the stroke attribute which by default does not appear.`

    	<line x1="0" y1="0"
    	          x2="500" y2="500"
    		  stroke="silver"
    	 />

    2. Let's add a second line that runs from the bottom left up to the upper right

    	○ What would the coordinates for that be?


    	<line x1="500" y1="0"
    	              x2="0" y2="500"
    	              stroke="black"
    	 />


    3. We can modify the stroke color, opacity and width. Let's add

```
<line x1="500" y1="0"
            x2="0" y2="500"
    stroke="#111"
            stroke-width="5"
            opacity=".5"
/>
```

---

### Circles:

Circles are very similar to rectangles. But rather than having a height or width, they have a radius r.

Also, their coordinates are set by the center of the triangle which is represented by cy="" and cx="" rather than x, y.

Let's put all of our SVG knowledge together to draw a circle that is:

○ on top of all our other elements
○ centered in the middle of our SVG
○ set the radius to 25px. r=""
○ give it a fill color of RGBA(255, 218, 185, .1) and
○ a stroke color of stroke="RGBA(219, 112, 147, .5)"
○ change the stroke width to 10px

```
<circle cx="250" cy="250" r="25" fill="RGBA(255, 218, 185, .1)" stroke="RGBA(219, 112, 147, .5)" stroke-width="10" />
```

---

### TEXT

    1. The text element is not self closing.
    2. The text style is inherited from the html document/css
    3. You can change it by using font-family and font-size
    4. You can place the text where ever you'd like by using x and y coordinates.

```
<text
    x="300"
    y="400"
    text-anchor="middle"
    transform="rotate(15)"
    font-size="50"
    stroke="indigo"
    opacity=".5">My Art</text>
```
