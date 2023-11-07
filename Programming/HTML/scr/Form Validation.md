## Introduction
Forms are one of the most critical parts of your site. They are your user's gateway into your back-end- the user provides data in a form, and you do stuff with it

### The form element

- The form element is a container element like the div element we learned earlier in the curriculum. The form element wraps all of the inputs a user will interact with on a form.

The form element accepts two essential attributes:

1. `action` attribute which takes a URL value that tells the form where it should send its data to be processed.
2. `method` attribute which tells the browser which [[HTTP Request Method]] it should use to submit the form. The **GET** and **POST** request methods are the two most used methods.

> [!NOTE] Note
> We use GET when we want to retrieve something from a server. For example, Google uses a **GET** request when you search as it *gets* the search results.
> 
> **POST** is used when we want to change something on the server, for example, when a user makes an account or makes a payment on a website

The markup for creating a form element looks like this:

```html
<form action="example.com/path" method="post">

</form>
```

### Form controls

To start collecting user data, we need to use form control element. These are all the elements users will interact with on the form, such as text boxes, drop downs, check boxes and buttons. 

#### The input element

The input element is the most versatile of all the form control elements. It accepts a `type` attribute which tells the browser what type of data it should expect and how it should render the input element.

Markup:
```html
<form action="example.com/path" method="post">
	<input type="text">
</form>
```

Hello