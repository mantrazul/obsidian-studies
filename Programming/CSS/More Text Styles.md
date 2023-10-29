# More Text Styles #CSS

## Introduction
More useful properties when working with text.

### Learning Outcomes
- Learn to use custom fonts on your web projects
- Learn some text-related CSS

[Cool thing](https://www.smashingmagazine.com/2020/07/css-techniques-legibility/)

#### Fonts

If you don't have the `font-family` it will be ugly. Because of that, people often list a lot of fonts as fallback.

```css
body {
  font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}

```

##### Online font libraries

- [Google Fonts](https://fonts.google.com/)
- [Font Library](https://fontlibrary.org/)
- [Adobe Fonts](https://fonts.adobe.com/)

```ad-abstract
title: Example of Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
```

Or using `@import`

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
```

##### Downloaded fonts

You can also use a custom font. You need to define it using `@font-face` and then use as any other font-family.

```ad-abstract
title: Example of custom-font

```css
@font-face {
  font-family: my-cool-font;
  src: url(../fonts/the-font-file.woff);
}

h1 {
  font-family: my-cool-font, sans-serif;
}
```


##### Text styles

###### font-style
```css
h1 {
  font-style: italic;
}
```

###### em

```html
<p>I <em>never</em> said he stole your money</p>
<p>I never said <em>he</em> stole your money</p>
<p>I never said he stole <em>your</em> money</p>
```

###### letter-spacing
Changes the space between letters.

###### line-height
Line height adjusts the space between lines in wrapped text. Adding a little line-height can increase readability.

###### text-transform
As you might expect, text-shadow adds a shadow around the text in the selected element. This one is best used sparingly, but can be used to great effect in headings or other presentational text.

###### ellipsis
This one isn’t a single property, but it’s a useful trick to keep in your toolbox. With the text-overflow property, you can truncate overflowing text with an ellipsis. Making an overflow happen, however, requires the use of a couple other properties because the default behavior of text simply printing outside its container isn’t technically considered an overflow (that’s confusing, we know. Sorry.)

The full snippet is:

```css
.overflowing {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

[Check this](https://css-tricks.com/snippets/css/truncate-string-with-ellipsis/)


