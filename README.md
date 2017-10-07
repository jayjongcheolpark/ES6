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

## `reduce` Helper

## `const` and `let`

## Template Strings

## Arrow Functions

## Enhanced Object Literals

## Default Function Arguments

## Rest and Spread Operator

## Destructuring

## Classes

## Generators

## Promises and Fetch