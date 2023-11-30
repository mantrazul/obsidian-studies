There are eight **Data Types**. Seven of them are called **primitive** because their value contain only a single thing.

In contrast, objects are used to store keyed collections of various data and more comple entities. In JavaScript, objects penetrate almost every aspect of the language. So we must understand them first before going in-depth anywhere else.

An object can be created with figure brackets `{...}` with an optional list of *properties*.

We can imagine an object as a cabinet with signed files. Every piece of data is stored in its file by the key. It's easy to find a file by its name or add/remove a file.

#### Object Literal

```javascript
let user = new Object();
let user = {};
```


### Literals and properties

We can put some properties into `{...}` as "key:value" pairs:

```javascript
let user = {       // an object
name: "John",      // by key "name" store value "john"
age: 30            // by key "age" store value 30
};
```

A property has a key (also known as a name or identifier) before the colon `:` and a value to the right of it.

In the `user` object, there are two properties:

1. The first property has the name "name" and the value "John"
2. The second one has the name "age" and the value `30`

The resulting `user` object can be imagined as a cabinet with two signed files labelled "name" and "age".

#### How to access properties
```javascript
alert( user.name ); // John
alert( user.age); // 30
```

The value can be any type. Let's add a boolean one:

```javascript
user.isAdmin = true
```