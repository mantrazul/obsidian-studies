### Anchor elements

To create a link in HTML, we use the anchor element. An anchor element is defined by wrapping the text or another HTML element we want to be a link with an `<a>` tag.

It needs a destination on where to go, and we do this by using an HTML attribute. An HTML attribute gives additional information to an HTML element and always goes in the element’s opening tag. An attribute is usually made up of two parts: a name, and a value; however, not all attributes require a value. In our case, we need to add a href (hypertext reference) attribute to the opening anchor tag. The value of the href attribute is the destination we want our link to go to.

```html
<a href="google.com">Click me<a/>
```

By default, any text wrapped with an anchor tag without a `href` attribute will look like plain text. If the `href` attribute is present, the browser will give the text a blue color and underline it to signify it is a link.
#### Opening links in a new tab
The method shown above opens links in the same tab as the webpage, this is the **default behaviour**. If we want to change that, there's the `target` attribute.

While `href` specifies the destination link, `target` specifies where the linked resource will be opened. If it is not present, then, by default, it will take on the `_self` value which opens the link in the current tab. To open the link in a new tab or window (depends on browser settings) you can set it to `_blank` as follows:

```html
<a href="https://www.theodinproject.com/about" target="_blank" rel="noopener noreferrer">click me</a>
```

You may have noticed that we snuck in the `rel` attribute above. This attribute is used to describe the relation between the current page and the linked document.

The `noopener` value prevents the opened link from gaining access to the webpage from which it was opened. The `noreferrer` value prevents the opened link from knowing which webpage or resource has a link (or ‘reference’) to it. It also includes the `noopener` behaviour and thus can be used by itself as well.

Why do we need this added behaviour for opening links in new tabs? Security reasons. The prevention of access that is caused by `noopener` prevents [phishing attacks](https://www.ibm.com/topics/phishing) where the opened link may change the original webpage to a different one to trick users. This is referred to as [tabnabbing](https://owasp.org/www-community/attacks/Reverse_Tabnabbing). Adding the `noreferrer` value can be done if you wish to not let the opened link know that your webpage links to it.

Note that you may be fine if you forget to add `rel="noopener noreferrer"` since more recent versions of browsers [provide this security](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#security_and_privacy) if only `target="_blank"` is present. Nevertheless, in line with good coding practices and to err on the side of caution, it is recommended to always pair a `target="_blank"` with a `rel="noopener noreferrer"`.

### Absolute and relative links

Generally, there are two kinds of links we will create:

1. Links to pages on other websites on the internet
2. Links to pages located on our own websites

#### Absolute links
Links to pages on other websites are called **absolute links**. A typical absolute link will be made up of the following parts: `protocol://domain/path`

#### Relative links
Links to pages on our website are called **relative links**. Relative links do not include the domain name, since it is another page on the same site, it assumes the domain name will be the same as the page we created the link on.

Relative links only include the file path to the other page, *relative* to the page you are creating the link on. This is quite abstract, let's see this in action using an example.

So, if you have a page inside a `pages/` directory, and want to link it via `<a>` you should do something like:

```html
<body>
  <h1>Homepage</h1>
  <a href="pages/about.html">About</a>
</body>
```

In many cases, this will work just fine; however, you can still run into unexpected issues with this approach. Prepending `./` before the link will in most cases prevent such issues. By adding `./` you are specifying to your code that it should start looking for the file/directory _relative_ to the `current` directory.

```html
<body>
  <h1>Homepage</h1>
  <a href="./pages/about.html">About</a>
</body>
```

### Images

To display an image in HTML, we use the `<img>` element. Unlike other elements we have encountered, the `<img>` element is **self-closing**. Empty, self-closing HTML elements do not need a closing tag.

You need the `scr` attribute for it to work like:
```html
<img src="https://www.theodinproject.com/mstile-310x310.png">
```

Using **relative paths** it stays like this:

```html
<body>
  <h1>Homepage</h1>
	<a href="https://www.theodinproject.com/about">click me</a>

	<a href="./pages/about.html">About</a>

	<img src="./images/dog.jpg">
</body>
```

### Parent directories

What if we want to use the dog image in the about page? We would first have to go up one level out of the pages directory into its parent directory so we could then access the images directory.

To go to the parent directory we need to use two dots in the relative filepath like this: `../`. Let’s see this in action, within the body of the `about.html` file, add the following image below the heading we added earlier:

```html
<img src="../images/dog.jpg">
```

To break this down:

1. First, we are going to the parent directory of the pages directory which is `odin-links-and-images`.
2. Then, from the parent directory, we can go into the `images` directory.
3. Finally, we can access the `dog.jpg` file.

Using the metaphor we used earlier, using `../` in a filepath is kind of like stepping out from the room you are currently in to the main hallway so you can go to another room.

#### Alt attribute
Besides the `src` attribute, there's the `alt` (alternative text) used to describe an image. It will be used in place when a image cannot be loaded or for **visually impaired users**

#### Image size attributes
While not strictly required, specifying height and width attributes in image tags helps the browser layout the page without causing the page to jump and flash.

It is a good habit to always specify these attributes on every image, even when the image is the correct size or you are using CSS to modify it.
