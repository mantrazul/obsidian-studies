# Emmet #emmet

## Introduction
Emmet is a puglin that is built into VS CODE that help you write code faster.

### Learning Outcomes
- Use some of Emmet's most useful shortcuts
- Set up custom Emmet keybindings in VS Code

#### Commands

Here are the main commands.

| Emmet                     | What it Does                 |
| ------------------------- | ---------------------------- |
| !   and !!!!              | Boilerplate                  |
| Shift + Ctrl + A          | Wrapper                      |
| Ctrl + K                  | Remove Tag                   |
| Ctrl + D                  | Balance                      |
| Ctrl + Alt + ->           | Next Edit Point              |
| lorem                     | Expand Lorem Ipsum           |
| Ctrl + M Ctrl + M         | Go to matching pair          |
| Ctrl + M Ctrl + Backspace | Remove Tag 2                 |
| Ctlr + M Ctrl + L         | Wrap Lines with Abbreviation | 

 - [Cheat-Sheet](https://docs.emmet.io/cheat-sheet/)
 - [Documentation](https://docs.emmet.io/)
 - [Lesson](https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-emmet)
- [Cool link](https://marketplace.visualstudio.com/items?itemName=agutierrezr.emmet-keybindings)
#### Summary

- If you type the name of the html tag it will auto fill
	- `span` will turn into `<span></span>`
- If you put `tag.class` you will create a CSS class, same with # for ids
- You can add attributes with `button[type="button"]`
- If you don't put anything it will create a `div`
- The `>` symbol is for child `div.purple>span.cyan`
	- Will result in `<div class="purple"><span class="cyan"></span></div>`
- If you put `*li*3{text $}` then you will create three elements; The $ introduces number.
- To create siblings just do `header+main+footer`
- To create siblings with a child just do `header>nav^main+footer`
	- You can this also as `(header>nav)+main+footer`



##### Wrapper Examples #wrapper
> [!example]
> .wrapper>h1{Title}+.content

```html
<div id="page">
	<p>Hello World</p>
</div>
```

```html
<div id="page">
    <div class="wrapper">
    	<h1>Title</h1>
    	<div class="content">
    		<p>Hello world</p>
    	</div>
    </div>
</div>
```

##### Individual line Examples #wrapper
> [!example]
> nav>ul.nav>li.nav-item$*>a

```html
<div id="page">
	About
	News
	Product
	Contact

	Lore ipsum dolor sit amet
</div>
```

```html
<div id="page">
<nav>
	<ul class="nav">
		<li class="nav-item1"><a href="">About</a></li>
		<li class="nav-item2"><a href="">News</a></li>
		<li class="nav-item3"><a href="">Products</a></li>
		<li class="nav-item4"><a href="">Contact</a></li>
	</ul>
</nav>
		Lore ipsum dolor sit amet
</div>
```

##### Removing list markers #wrapper
> [!example]
> ul.nav>li.nav-item$*>a|t

```html
<div id="page">
	1. About
	2. News
	3. Product
	4. Contact

	Lore ipsum dolor sit amet
</div>
```

```html
<div id="page">
    
    <ul class="nav">
    	<li class="nav-item1"><a href="">About</a></li>
    	<li class="nav-item2"><a href="">News</a></li>
    	<li class="nav-item3"><a href="">Products</a></li>
    	<li class="nav-item4"><a href="">Contacts</a></li>
    </ul>

    Lorem ipsum dolor sit amet.
</div>
```

##### Controlling output position #wrapper
> [!example]
>  `ul>li[title=$#]*>{$#}+img[alt=$#] ` 

```html
<div id="page">
	About
	News
	Product
	Contact

	Lore ipsum dolor sit amet
</div>
```

```html
<div id="page">
    
    <ul>
    	<li title="About">About<img src="" alt="About"></li>
    	<li title="News">News<img src="" alt="News"></li>
    	<li title="Products">Products<img src="" alt="Products"></li>
    	<li title="Contacts">Contacts<img src="" alt="Contacts"></li>
    </ul>

    Lorem ipsum dolor sit amet.
</div>
```

##### Remove Tag #remove_tag
> [!example]
>  `ctrl + k` 

```html
<body>
	<div class="wrapper"> // place it here
	    <h1>Title</h1>
	    <p>Lorem ipsum dolor sit amet.</p>
	    <p>Officiis animi consequuntur iure.</p>
	    <p>Ea asperiores aperiam non necessitatibus?</p>
	    <p>Expedita iusto cupiditate eum esse.</p>
	</div>
</body>
```

```html
<body>
    <h1>Title</h1>
    <p>Lorem ipsum dolor sit amet.</p>
    <p>Officiis animi consequuntur iure.</p>
    <p>Ea asperiores aperiam non necessitatibus?</p>
    <p>Expedita iusto cupiditate eum esse.</p>
</body>
```