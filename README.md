# Arrays
In the context of Javascript Arrays are list-like objects. It is similar to what other languages might call a list, stack, or a queue.

Arrays are used to store multiple values in a single variable.

## Declaring an Array
You are able to declare an Array in one of two ways:

Array Constructor:
```js
let array1 = new Array(1, 2, 3)
```
Here we are able to utilize the `new` keyword along with the `Array` constructor to create a new Array. We then pass three arguments `1, 2, 3` into the constructor a new array is created with the given elements.

						OR

Array Literal Notation:
```js
let array1Clone = [1, 2, 3]
```
The literal notation is the most widely used syntax over the two options. With it you are able to define a variable name and set its value to an Array by utilizing the bracket operator.

There is no reason to use the Array Constructor `new Array()`. Both example do exactly the same thing. The Array literal method is simple, more readably, and has faster execution speed.

## Accessing
You access an Array with the brackets operator `[]`.   Each item stored in an array is house in an index. We use zero-based indices to access an Array in Javascript, meaning an Array’s first index starts at `0`.

```js
console.log(array1[0]) // output: 1
```

## Changing an Array Element
You are able to change an Array’s index by doing the follow:

```js
let gardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

gardians[4] = 'Thor'
```







#CodeDifferently