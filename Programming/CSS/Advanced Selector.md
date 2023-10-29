# Advanced Selectors #CSS

## Introduction
This selectors should meet the need of more precision if you don't want to mess with the html.

There are a *lot* of advanced selectors, and going through every single one would be beyond the scope of this project.

### Learning Outcomes
- Understand how to use parent and sibling selectors
- Recognize the difference between pseudo classes and pseudo elements
- Learn about some of the most useful and common pseudo elements and pseudo classes
- Learn about the different ways to select an attribute or its parts

### Child and sibling combinators

Let's have a look at some more ways we can access different elements without reffering to their classes. 

- `>` - the child combinator
- `+` - the adjacent sibling combinator
- `~` - the general sibling combinator
- 
Consider the following HTML

```html
<main class="parent">
  <div class="child group1">
    <div class="grand-child group1"></div>
  </div>
  <div class="child group2">
    <div class="grand-child group2"></div>
  </div>
  <div class="child group3">
    <div class="grand-child group3"></div>
  </div>
</main>
```

If I wanted to write a rule that select all the `child` and `grand-child` inside `main`

```CSS
main div {
/*CSS*/
}
```

But what if we wanted to select only the `child` or `grand-child` divs? Well, that's what the *`>`* combinator is for.

```CSS

/* This rule will only select divs with a class of child */
main > div {
  /* Our cool CSS */
}

/* This rule will only select divs with a class of grand-child */
main > div > div {
  /* More cool CSS */
}
```

The child selector will select an element that is one level of indentation down. If it's adjacent you can use the *adjacent* sibling combinator `+`

```
/* This rule will only select the div with the class child group2 */
.group1 + div {
  /* Our cool CSS */
}

/* This rule will only select the div with the class child group3 */
.group1 + div + div {
  /* More cool CSS */
}
```

And finally if you want to select all the siblings of an element you can use the *general* sibling combinator `~`

```CSS
/* This rule will select all of .group1's siblings - in this case the 2nd and 3rd .child divs */
.group1 ~ div {
  /* Our cool CSS */
}
```

[Read More](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators)

### Pseudo-selectors

Quick note between pseudo-elements and pseudo-classes.

1. Pseudo-classes selectors are prefixed with a single colon and are a different way to target elements that already exist in HTML.
2. Pseudo-elements are prefixed with two colons and are used to target elements that *don't* usually exist in the markup.

#### Pseudo-classes
Pseudo-classes offer us different ways to target elements in out HTML. 

Example of pseudo-classes:
```CSS
/* Any button over which the user's pointer is hovering */
button:hover {
  color: blue;
}
```

Note: it should be followed by `:`

[Read More](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

```ad-note
title: Note: Specifics on CSS Specificity

Here's a simple unordered list:

```html
<ul id="summer-drinks">
   <li>Whiskey and Ginger Ale</li>
   <li>Wheat Beer</li>
   <li>Mint Julip</li>
</ul>
```d

Now you want to designate one of these your favorite frink and change its styling a bit.

```HTML
<ul id="summer-drinks">
   <li class="favorite">Whiskey and Ginger Ale</li>
   <li>Wheat Beer</li>
   <li>Mint Julip</li>
</ul>

```CSS

Now you open your CSS and do your styling for your new class.

```CSS
.favorite {
  color: red;
  font-weight: bold;
}
```CSS

Poking around you find this:

```CSS
ul#summer-drinks li {
   font-weight: normal;
   font-size: 12px;
   color: black;
}
```CSS

Two different CSS selectors are telling that text what colour and font-weight to be. There's only one statement for font-size, so clearly one will take effect. These aren't "conflicts" per-say, but the browser does need to decide which one of these statements to  honour.

The point here is that you *want to be specific as it makes sense to be* every chance you get. So you should use:

```CSS
ul#summer-drinks li.favorite {
  color: red;
  font-weight: bold;
}

//or this

html body div#pagewrap ul#summer-drinks li.favorite {
  color: red;
  font-weight: bold;
}

```CSS

You can always add an `!important` which is like a Jedi mind trick for CSS

```CSS
.favorite {
  color: red !important;
  font-weight: bold !important;
}
```
![[Pasted image 20230728194056.png]]

- If the element has inline styling, that automatically 1 wins (1,0,0,0 points)
- For each ID value, apply 0,1,0,0 points
- For each class value (or pseudo-class or attribute selector), apply 0,0,1,0 points
- For each element reference, apply 0,0,0,1 point
[Read again if in doubt](https://css-tricks.com/specifics-on-css-specificity/)

#### Dynamic and user action pseudo-classes

These types of useful pseudo-classes can make your page feel much more dynamic and interactive.

##### :focus
Applies to an element that is currently selected by the user either through selecting it with their cursor or using their keyboard.

##### :hover
Will affect anything under the user’s mouse pointer. It can be used to give extra oomph to buttons and links to highlight that they’re interactable, or to trigger a drop-down menu.

##### :activate
applies to elements that are currently being clicked, and is especially useful for giving your user feedback that their action had an effect. This is a great one to give your buttons and other interactive elements more ‘tactile’ feedback.

##### :visited and :link
Have you ever wondered why links are blue but turn purple when clicked in unstyled HTML? It’s because browsers implement that styling by default. To implement your own custom styling for links, take advantage of the :link and :visited pseudo-classes. A simplified version of default browser styling might look something like this:

```CSS
  /* This rule will apply to all links */
  a {
    text-decoration: underline;
  }

  /* This will apply to unvisited links */
  a:link {
    color: blue;
  }

  /* And you guessed it, this applies to all links the user has clicked on */
  a:visited {
    color: purple;
  }
```

#### Structural pseudo-classes

##### :root

Is a special class that represents the very top level of your document - the one element that has no parents. Generally when working with the web, this is equivalent to the html element, but there are a [few subtle differences](https://stackoverflow.com/questions/15899615/whats-the-difference-between-css3s-root-pseudo-class-and-html)

It is generally the place where you ill place your 'global' CSS rules that you want avaiable everywhere - such as your custom properties and CSS variables or rules such as `box-sizing: border-box`.

##### :first-child and :last-child

Will match elements that or either the first or last sibling. 

##### :empty

Will match elements that have no children at all.

##### :only-child

Will match elements that don't have any siblings.

##### :nth-child

This is a flexible pseudo-class with a few different uses.

```CSS

  .myList:nth-child(5) {/* Selects the 5th element with class myList */}

  .myList:nth-child(3n) { /* Selects every 3rd element with class myList */}

  .myList:nth-child(3n + 3) { /* Selects every 3rd element with class myList, beginning with the 3rd */}

  .myList:nth-child(even) {/* Selects every even element with class myList */}
```

### Pseudo-elements

While pseudo-classes give us an alternative way to interact with out HTML elements based on their state or structure, *pseudo-elements* are more abstract.

They allow us to affect parts of our HTML that aren't elements at all. These special elements share the same specificity as regular elements (0, 0, 0, 1). There are a number of useful pseudo-elements that can be utilised in any number of creative ways.

##### ::marker
Allows you to customize the styling of your `<li>` elements' bullets or numbers.

##### ::first-letter and ::first-line
Allows you to give special styling to the first letter or line of some text.

##### ::selection
Allows you to change the highlighting when a user selects text on the page.

##### ::before and ::after
Allows us to add extra elements onto the page with CSS, instead of HTML. Using it to decorate text in various ways is one common use case.

```CSS
<style>
  .emojify::before {
    content: '😎 🥸 🤓';
}

  .emojify::after {
    content: '🤓 🥸 😎';
}
</style>

<body>
  <div> Let's <span class="emojify">emojify</span>this span!</div>
</body>
```

[Read More](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)
