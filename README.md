# ES6 Javascript

## `forEach` Helper

```js
var numbers = [1,2,3,4,5]
var sum = 0

function adder(number) {
  sum += number
}

numbers.forEach(adder)
```

## `map` Helper

```js
var numbers = [1,2,3]

var doubledNumbers = numbers.map(
  number => { return number * 2 }
)
```

```js
var paints = [ { color: 'red' }, { color: 'blue' }, { color: 'yellow' }];
pluck(paints, 'color'); // returns ['red', 'yellow', 'blue'];

function pluck(array, property) {
    return array.map(elem => {
       return elem[property];
    });
}
```

## `filter` Helper

```js
var post = { id: 4, title: 'New Post' }

var comments = [
  { postId: 4, content: 'awesome post' },
  { postId: 3, content: 'it was ok' },
  { postId: 4, content: 'neat' }
]

function commentsForPost (post, comments) {
	return comments.filter(comment => {
  	return comment.postId === post.id
  })
}
```

```js
[{"postId":4,"content":"awesome post"},{"postId":4,"content":"neat"}]
```

## `find` Helper

```js
var users = [
  { name: 'Jill' },
  { name: 'Alex', id: 1 },
  { name: 'Alex' }
]

users.find(user => {
  return user.name === 'Alex'
})
// {"name":"Alex","id":1}

users.filter(user => {
  return user.name === 'Alex'
})
// [{"name":"Alex","id":1},{"name":"Alex"}]
```

## `every` and `some` Helper

```js
var computers = [
  { name: 'Apple', ram: 24},
  { name: 'Compaq', ram: 4},
  { name: 'Acer', ram: 32}
]

computers.every(computer => {
  return computer.ram > 16
})
// false

computers.some(computer => {
  return computer.ram > 16
})
// true
```

```js
function Field(value) {
  this.value = value
}

Field.prototype.validate = function() {
  return this.value.length > 0
}

var username = new Field("Jay")
var password = new Field("1234")
var birthdate = new Field("10/10/2010")

var fields = [username, password, birthdate]
fields.every(function(field) {
  return field.validate()
})
// true
```

## `reduce` Helper

```js
var numbers = [10,20,30]
var sum = 0

numbers.reduce((sum, number) => {
  return sum + number
}, 0)
// 60
```

```js
var primaryColors = [
  { color: 'red'},
  { color: 'yellow'},
  { color: 'blue'}
]

primaryColors.reduce((previous, primaryColor) => {
	previous.push(primaryColor.color)
  return previous
}, [])
// ["red","yellow","blue"]
```

```js
function blancedParens(string) {
	return !string.split("").reduce((previous, char) => {
  	if (previous < 0) { return previous }
    if (char === "(") { return ++previous }
  	if (char === ")") { return --previous }
  	return previous
  }, 0)
}

blancedParens("((((") // false
blancedParens("(())") // true
```

```js
function unique(array) {
  return array.reduce(
    (uniques, elem) =>
    uniques.find(el => el === elem)
    ? uniques : [...uniques, elem], []
  )
}

var numbers = [1, 1, 2, 3, 4, 4]

unique(numbers) // [1,2,3,4]
```

## `const` and `let`

```js
{
	const a = 2;
	console.log( a );	// 2

	a = 3;				// TypeError!
}
```

```js
{
	const a = [1,2,3];
	a.push( 4 );
	console.log( a );		// [1,2,3,4]

	a = 42;					// TypeError!
}
// If the value is complex, such as an object or array,
// the contents of the value can still be modified
```

```js
var a = 2;

{
	let a = 3;
	console.log( a );	// 3
}

console.log( a );		// 2
```

## Template Strings

```js
function getMessage() {
  const year = new Date().getFullYear()
  return `The year is ${year}`
}
```

## Arrow Functions

## Enhanced Object Literals

## Default Function Arguments

## Rest and Spread Operator

## Destructuring

## Classes

## Generators

## Promises and Fetch