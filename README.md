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

# Something
