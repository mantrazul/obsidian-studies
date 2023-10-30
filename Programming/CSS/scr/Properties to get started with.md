
CSS fundamental properties that will allow you to do the basics.

#### color and background-color

The `color` property sets an element's text colour while `background-color` set the background colour of an element.

```css
p {
  /* hex example: */
  color: #1100ff;
}

p {
  /* rgb example: */
  color: rgb(100, 0, 127);
}

p {
  /* hsl example: */
  color: hsl(15, 82%, 56%);
}
```

#### Typography basics and text-align

`font-family` can be a single value or a comma-separated list of values that determine what font an element uses. Each font will fall into one of two categories, either a "font family name" like `"Times New Roman"` (we use quotes due to the white-space between words) or a "generic family name" like `sans-serif` (generic family names never use quotes)

If a browser cannot find or does not support the first font in the list, it will use the next one and so on. Always have a generic font family as fallback, e.g. `font-family: "Times New Roman", sans-serif;`

`font-size` will set the size of the font. -> `font-size: 22px;`. Remember to use another metrics.

`font-weeight` affect the boldness of text assuming it supports it. It can be a keyword, `font-weight: bold;` or a number between 1 and 1000 e.g. `font-weight: 700` (the equivalent of `bold`). Usually, the numeric values will be in increments of 100 up to 900.

`text-align` will align text horizontally within an element, and you can use the common keywords found on word processors;

#### Image height and width

By default, an `<img>` element's `height` and `width` values will be the same as the actual image file's height and width. If you wanted to adjust the size of the image without causing it to lose its proportions, you would use the value of  `auto` for the `height` property and adjust the `width`.

```css
img {
  height: auto;
  width: 500px;
}
```

For example, if an image’s original size was 500px height and 1000px width, using the above CSS would result in a height of 250px.

> [!IMPORTANT] About image's size
> It’s best to include both of these properties for `<img>` elements, even if you don’t plan on adjusting the values from the image file’s original ones. When these values aren’t included, if an image takes longer to load than the rest of the page contents, the image won’t take up any space on the page at first, but will suddenly cause a drastic shift of the other page contents once it does load in. Explicitly stating a `height` and `width` prevents this from happening, as space will be “reserved” on the page and will just appear as a blank space until the image loads.
