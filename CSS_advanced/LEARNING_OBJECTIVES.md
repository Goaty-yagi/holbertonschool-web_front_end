# Learning Objectives

- [Selectors, properties, and values](#Selectors,-properties,-and-values)
- [The difference between block and inline styling](#The-difference-between-block-and-inline-styling)
- [How to ensure consistency across all browers (CSS reset)](#How-to-ensure-consistency-across-all-browers-(CSS reset))
- [How to setup CSS variables](#How-to-setup-CSS-variables)
- [The differences between inline, embeded and external CSS](#The-differences-between-inline,-embeded-and-external-CSS)
- [How grid systems work (with floats)](#How-grid-systems-work "with floats")
- [The difference between icons webfonts and SVG icons](#The-difference-between-icons-webfonts-and-SVG-icons)
- [The difference between pseudo-classes and pseudo-elements](#The-difference-between-pseudo-classes-and-pseudo-elements)
- [How to make background gradients](#How-to-make-background-gradients)
- [How to animate elements in CSS](#How-to-animate-elements-in-CSS)
- [How to transform (2d, 3d) elements](<#How-to-transform-(2d,3d)-elements>)
- [What vendor prefixes are](#What-vendor-prefixes-are)

## Selectors, properties, and values

```css
/* CSS Rule */
p {
  color: blue; /* Selector: p, Property: color, Value: blue */
}

/* CSS attribute selector */
[data-section-theme="dark"] {
    --text-color: white;
    --section-title-color: white;
    background: var(--color-black);
}
<body data-section-theme="dark"></body>
```

## The difference between block and inline styling

### Block-level Elements:

- Display Behavior:
  -- Block-level elements typically start on a new line and stretch the full width of their parent container, creating a "block" of content.
- Examples:
  -- <div>, <p>, <h1> to <h6>, <ul>, <li>, <table>, etc.
- CSS Properties:
  -- width and height can be set.
  -- margin, padding, and border properties apply to all four sides.

### Inline Elements:

- Display Behavior: 
-- Inline elements do not start on a new line, and they only take up as much width as necessary. 
-- They flow along with the content.
- Examples:
-- <span>, <a>, <strong>, <em>, <img>, <br>, etc.
- CSS Properties:
-- width and height are ignored.
-- Horizontal properties like margin-left, margin-right, padding-left, and padding-right apply.

### Inline Block Elements:
- Combines aspects of both block and inline elements. 
- Inline-block elements flow horizontally like inline elements but can have width, height, margins, padding, and borders like block elements. Examples of inline-block elements include <img> and <button>.

## How to ensure consistency across all browers (CSS reset)
```css
/* Eric Meyer's CSS Reset - Reset.css */
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}

/* Add your custom styles below this line */

```

or 

```css
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css" integrity="sha256-l7X2gkoqz5OXPrYnDEuT5f2JWwFOQjcH5AnAYTiUeI0=" crossorigin="anonymous">

```

## How to setup CSS variables

### Declaration:
- Define your CSS variables within a selector, such as the :root pseudo-class, which represents the root element (usually the <html> element).

```css
:root {
  --primary-color: #3498db;
  --font-size: 16px;
}
```

In this example, --primary-color and --font-size are the CSS variables, representing a color and a font size, respectively.

### Usage:

To use a CSS variable, reference it using the var() function.
```css
body {
  background-color: var(--primary-color);
  font-size: var(--font-size);
}
```

### Updating Variables:

CSS variables are dynamic, and you can update their values using JavaScript or media queries. This flexibility allows for easy theming and responsive design.

```css
document.documentElement.style.setProperty('--primary-color', '#ff5733');

```

```css
@media (max-width: 600px) {
  :root {
    --font-size: 14px;
  }
}
```

## The differences between inline, embeded and external CSS
- Inline CSS:
the style in the HTML tag

- Embedded (Internal) CSS:
the style in the HTML file

External CSS:
the style sheet with extension .css

## How grid systems work (with floats)
Grid systems using floats were a popular method for creating layouts in the early days of web development before modern layout techniques like CSS Grid and Flexbox were widely adopted. 

## The difference between icons webfonts and SVG icons

Styling property are different

## The difference between pseudo-classes and pseudo-elements
Pseudo-classes and pseudo-elements are both types of selectors in CSS, but they serve different purposes and target different parts of an element's state or structure.

### Pseudo-classes:
```css
/* Example: Hover state */
a:hover {
  color: #FF0000;
}
```
#### Examples:
- :hover, :active, :focus: Target elements based on user interaction.
- :nth-child(), :nth-of-type(): Select elements based on their position within a parent.
- :first-child, :last-child: Select the first or last child of a parent. 

### Pseudo-elements:
```css
/* Example: Styling the first line of a paragraph */
p::first-line {
  font-weight: bold;
}
```

### Examples:

- ::before, ::after: Insert content before or after the content of an element.
- ::first-line, ::first-letter: Style the first line or letter of a block-level element.
- ::selection: Style the selected text.


## How to make background gradients
1, to bottom right left
2, circle
```css
body {
  background: linear-gradient(to bottom, #ffcc00, #ff3300);
}

```
## How to animate elements in CSS

### transition
```css
/* Define the initial state */
.element {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 0.5s, height 0.5s, background-color 0.5s;
}

/* Define the hover state */
.element:hover {
  width: 150px;
  height: 150px;
  background-color: red;
}
```

### CSS Animations:
```css
/* Define the animation */
@keyframes scaleAndColorChange {
  0% {
    transform: scale(1);
    background-color: blue;
  }
  50% {
    transform: scale(1.5);
    background-color: red;
  }
  100% {
    transform: scale(1);
    background-color: blue;
  }
}

/* Apply the animation to the element */
.element {
  width: 100px;
  height: 100px;
  background-color: blue;
  animation: scaleAndColorChange 2s infinite; /* animation-name, duration, iteration count */
}

```
## How to transform (2d, 3d) elements
### 2D Transformations:
- Translate (Move):
```css
.element {
  transform: translate(50px, 20px);
}
```

- Scale (Resize):
```css
.element {
  transform: scale(1.5); /* Increase size by 1.5 times */
}
```
- Rotate:
```css
.element {
  transform: rotate(45deg);
}

```

- Skew:
```css
.element {
  transform: skew(30deg, 20deg);
}

```
- Combined 2D Transformations:
```css
.element {
  transform: translate(50px, 20px) rotate(45deg) scale(1.5);
}
```

### 3D Transformations:
- Translate (Move):
```css
.element {
  transform: translate3d(50px, 20px, 30px);
}
```

- Scale (Resize):
```css
.element {
  transform: scale3d(1.5, 1.2, 0.8);
}
```

- Rotate:
```css
.element {
  transform: rotate3d(1, 1, 1, 45deg); /* Rotate around the vector (1, 1, 1) by 45 degrees */
}
```
- Perspective (3D Effect):
```css
.container {
  perspective: 1000px; /* Set the perspective value */
}

.element {
  transform: rotateY(45deg);
}
```

- Combined 3D Transformations:
```css
.element {
  transform: translate3d(50px, 20px, 30px) rotate3d(1, 1, 1, 45deg) scale3d(1.5, 1.2, 0.8);
}
```
## What vendor prefixes are
Vendor prefixes are prefixes added to CSS property names to identify the specific browser that the rule is intended for.

```css
.element {
  -webkit-border-radius: 10px; /* Chrome, Safari, newer versions of Edge */
  -moz-border-radius: 10px;    /* Firefox */
  -o-border-radius: 10px;      /* Opera */
  -ms-border-radius: 10px;     /* Internet Explorer, Microsoft Edge */
  border-radius: 10px;         /* Standard property */
}
```