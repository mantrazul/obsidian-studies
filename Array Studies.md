
`Array.prototype.filter()`

Examples:

```javascript
fruits = ['banana', 'apple', 'orange']

fruits.filter((word) => word.length > 6)

function isBigEnough(value) {
	return value >= 10;
}

const filtered = [12, 5, 6, 130, 44].filter(isBigEnough);
```

#### Anonymous Functions

An anonymous function is a function without a name. The following shows how to define a anonymous function:

```javascript
(function() {}
})
```

An anonymous function is not accessible after its initial creation. Therefore, you often need to assign it to a variable.

```javascript
let show = function() {
console.log('Anonymous function';)
}
```

In practice, you often pass anonymous functions as arguments to other functions. For example:

```javascript
setTimeout(function() {
	console.log('Execute later after 1 second')
}, 1000)
```

If you want to create a function and execute it immediately after the declaration, you can declare an anonymous function like this:

```javascript
function() {
	console.log('TIFE')
}();

//with arguments

function() {
	console.log(person.FirstName +' '+ person.lastName); 
}(person)
```

#### Arrow functions

```javascript
let show = function() {
	console.log('Anonymous function');
}
```

Can become

```javascript
let show = () => console.log('Anonymous function');
```

or
```javascript
let add = function(a, b) {
	return a + b
}
```