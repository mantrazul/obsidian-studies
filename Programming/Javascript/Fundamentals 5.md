## Fundamentals Part 5 #object #javascript

- Creating objects
- Acessing object properties
- Being able to use multiple object operators
- Being able to use more powerful array functions.

### Objects

There are eight [[Data types]]. Seven of them are called "primitive" because *their values contain only a single thing*.
In contrast, objects are used to store keyed collections of various data and more complex entities.

An object can be created in the following way, using `{...}` that is called a *object literal*

```javascript
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```

### Literals and properties

We can put some properties into `{...}` into key/pair things.
```javascript
let user = {     // an object
  name: "John",  // by key "name" store value "John"
  age: 30        // by key "age" store value 30
};
```

A property has a *key* (also known as "name" or "identifies") before the `:` and a value to the right of it.

In the `user` object, there are two properties:
1. The first property has the name `name` and the value `John`.
2.  The second one has the name `age` and the value `30`.

You can acess the properties with *dot notation*.

```javascript
// get property values of the object:
alert( user.name ); // John
alert( user.age ); // 30
```

And they can be boolean too, alongside how to delete it

```javascript
user.isAdmin = true;

delete user.age;
```

If you wish to use multi-property you can like this:

```javascript
let user = {
  name: "John",
  age: 30,
  "likes birds": true  // multiword property name must be quoted
};
```

You may end the last setence with a comma to facilitate future insertations, this is called "trailling" or "hanging" comma.

### Square brackets

For multiword properties the dot notation doesn't work so use this instead.

```javascript
// this would give a syntax error
user.likes birds = true
```

The dot requires the key to be a valid varaible identifier. So it must:
- contain no spaces
- doesn't start witha  digit
- doesn't include special characters ($ and _ are allowed).

The alternative is the *square bracket notation*.

```javascript
let user = {};

// set
user["likes birds"] = true;

// get
alert(user["likes birds"]); // true

// delete
delete user["likes birds"];
```

And you can access the property name as a result of any expression.

```javascript
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```

Here, the variable `key` may be calculated at run-time or depend on the user input. And then we use it to acess the property. That give us a great deal of flexibility.

For example:

```javascript
let user = {
  name: "John",
  age: 30
};

let key = prompt("What do you want to know about the user?", "name");

// access by variable
alert( user[key] ); // John (if enter "name")
```

```ad-info
title: Important
The dot notation cannot be used in a similar way!!

```
