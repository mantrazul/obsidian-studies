****
#CSS 
### Flex direction

By default, items will stack side-by-side in a row, but we can flip to a column with the `flex_direction` property.

Column -> Primary Axis is **Vertical** (top to bottom)
Row -> Primary Axis is **Horizontal** (left to right)

![[Pasted image 20240208174230.png]] ![[Pasted image 20240208174245.png]]

Primary axis -> `justify-content'
Cross-axis -> `align-items`

## Align-self
It's only to the child.

### Real questions

When we're talking about alignment in the _cross_ axis, each item can do whatever it wants. In the _primary_ axis, though, we can only think about how to distribute the _group_.

### flex-basis
In a Flex row, `flex-basis` does the same thing as width. In a Flex column the same thing as height.

As we've learned, everything in Flexbox is _pegged to the primary/cross axis_. For example, `justify-content` will distribute the children along the primary axis, and it works exactly the same way whether the primary axis runs horizontally or vertically.

`width` and `height` don't follow this rule, though! `width` will always affect the horizontal size. It doesn't suddenly become `height` when we flip `flex-direction` from `row` to `column`.

**And so, the Flexbox authors created a generic “size” property called `flex-basis`.** It's like `width` or `height`, but pegged to the _primary axis_, like everything else. It allows us to set the _hypothetical size_ of an element in the primary-axis direction, regardless of whether that's horizontal or vertical.

### flex-grow
By default, elements in a Flex context will shrink down to their minimum comfortable size along the primary axis. This often creates extra space.

We can specify how that space should be consumed with the `flex-grow` property:
### flex-shrink

 `flex-grow` controls how the _extra space is distributed_ when the items are smaller than their container.
     
`flex-shrink` controls how _space is removed_ when the items are bigger than their container.

https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/