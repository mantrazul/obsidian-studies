# More CSS Properties #CSS

## Introduction
Here we will cover more useful tools for CSS. There are a lot of CSS properties. The amount you are going to be using in a daily basis is much smaller.

### Learning Outcomes
- Learn about (more) useful CSS properties

##### Properties

###### background

The background property is actually a shorthand for 8 different background-related properties, all of which you can read about. Beyond changing *background-colors* you can also specify background images repeat to tile if they are too small to fill the container.

It's *possible* to use this properties individually.

```CSS
/* Using a <background-color> */
background: green;

/* Using a <bg-image> and <repeat-style> */
background: url("test.jpg") repeat-y;

/* Using a <box> and <background-color> */
background: border-box red;

/* A single image, centered and scaled */
background: no-repeat center/80% url("../img/image.png");

/* Global values */
background: inherit;
background: initial;
background: revert;
background: revert-layer;
background: unset;
```

[Read More](https://developer.mozilla.org/en-US/docs/Web/CSS/background)
[CSS-TRICKS](https://css-tricks.com/almanac/properties/b/background/)

###### borders

The `border` property is another shorthand but not as much as background. The `border-radius` is the property used to create round corners.

```CSS
/* style */
border: solid;

/* width | style */
border: 2px dotted;

/* style | color */
border: outset #f33;

/* width | style | color */
border: medium dashed green;

/* Global values */
border: inherit;
border: initial;
border: revert;
border: revert-layer;
border: unset;
```

```CSS
/* The syntax of the first radius allows one to four values */
/* Radius is set for all 4 sides */
border-radius: 10px;

/* top-left-and-bottom-right | top-right-and-bottom-left */
border-radius: 10px 5%;

/* top-left | top-right-and-bottom-left | bottom-right */
border-radius: 2px 4px 2px;

/* top-left | top-right | bottom-right | bottom-left */
border-radius: 1px 0 3px 4px;

/* The syntax of the second radius allows one to four values */
/* (first radius values) / radius */
border-radius: 10px / 20px;

/* (first radius values) / top-left-and-bottom-right | top-right-and-bottom-left */
border-radius: 10px 5% / 20px 30px;

/* (first radius values) / top-left | top-right-and-bottom-left | bottom-right */
border-radius: 10px 5px 2em / 20px 25px 30%;

/* (first radius values) / top-left | top-right | bottom-right | bottom-left */
border-radius: 10px 5% / 20px 25em 30px 35em;

/* Global values */
border-radius: inherit;
border-radius: initial;
border-radius: revert;
border-radius: revert-layer;
border-radius: unset;
```

[Border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
[Border-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

###### box-shadow

It adds a shadow effect around an element. Can create a sense of depth if needed.

```CSS
/* Keyword values */
box-shadow: none;

/* offset-x | offset-y | color */
box-shadow: 60px -16px teal;

/* offset-x | offset-y | blur-radius | color */
box-shadow: 10px 5px 5px black;

/* offset-x | offset-y | blur-radius | spread-radius | color */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* inset | offset-x | offset-y | color */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow:
  3px 3px red,
  -1em 0 0.4em olive;

/* Global values */
box-shadow: inherit;
box-shadow: initial;
box-shadow: revert;
box-shadow: revert-layer;
box-shadow: unset;
```

[Read More](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)

###### overflow

This is most used to define what happens to a element when its content is too big to fit. Most common usage includes to add scrollbars to an element inside a web page, for example a card element with scrollable content.

```CSS
overflow = 
  [ visible | hidden | clip | scroll | auto ]{1,2} 
```

[Read More](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)
[CSS-tricks](https://css-tricks.com/almanac/properties/o/overflow/)

###### opacity

Noteworth is that is that min 0 and max 1.

[Duh](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity)

