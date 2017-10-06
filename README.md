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
var products = [
  { name: 'cucumber', type: 'vegetable' },
  { name: 'banana', type: 'fruit' },
  { name: 'celery', type: 'vegetable' },
  { name: 'orange', type: 'fruit' }
]

const isFruit = ({ type }) => { return type === 'fruit' }

products.filter(isFruit)
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