# Arrays
In the context of Javascript Arrays are list-like objects. It is similar to what other languages might call a list, stack, or queue.

Arrays are used to store multiple values in a single variable.

## Declaring an Array
You are able to declare an Array in one of two ways:
1. Array Literal Notation - Defining a new array using `brackets` notation.
2. Array Constructor - Defining a new array using the `new Array()` syntax

### Array Literal Notation:

The literal notation is the most widely used syntax over the two options.
With it you are able to:
1. Define a variable name
2. Set the variable's value to an Array by utilizing the bracket operator
3. Set values for any of the arrays indexes
```js
let array1 = [1, 2, 3]
console.log(array1) // output: (3) [1, 2, 3]
```

### Array Constructor:
The array constructor is the original syntax for instantiating an array. You are able to utilize in by declaring the `new` keyword along with the `Array` constructor to create a new Array.

```js
let array1 = new Array(1, 2, 3)
console.log(array2) // output: (3) [1, 2, 3]
```

Whereas the `array constructor` and the `array literal` perform the same take, meaning they both allow you to instantiate a new array.

The `constructor` syntax does allots you 1 extra feature. You are able to instantiate an array with blank index values:

```js
let emptyArray = new Array(3)
console.log(emptyArray) // output: (3) [empty × 3]
```


There is **no reason to use** the Array Constructor `new Array()`. Both example do exactly the same thing. The Array literal method is simple, more readably, and has faster execution speed.

## Accessing
You access an Array with the brackets operator `[]`. Each item stored in an array is house in an index. We use zero-based indices to access an Array in Javascript, meaning an Array’s first index starts at `0`.

```js
let array 1 = ['I am located in index 0', 'I am located in index 1', 'I am located in index 2', ]
console.log(array1[0]) // output: 1
```

## Changing an Array Element
You are able to change an Array’s index by accessing it by its zero based location and then resetting its value:

```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

console.log(guardians[2]) // output: ['Gamora']

guardians[2] = 'Thor'

console.log(guardians[2]) // output: ['Thor']

console.log(guardians) // Outputs: [ 'Groot', 'Star Lord', 'Thor', 'Mantis']

```
## Arrays are Objects
Whereas Arrays are objects they are considered a special type of object and in turn are described as arrays. If you use the `typeof` operator on an Array it will returns `"objects"`.

```js
let array = []

typeof(array) // Outputs: "object"
```


## The Length Property
The `length` property returns the total number of indices stored in an array.

```js
let sg1 = ["Teal'c", "Carter", "O'Neill", "Jackson"]
sg1.length //outputs: 4
```
Where as the index of an Array is accessed using zero-based indices we could the length property

## Interacting with Arrays
Arrays are meant to store multiple values in a single variable. But what can you do with an Array once you create one and store some data in it?

### Iterating Over an Array
Two options to start with are a `for loop` and the `forEach` method.

#### For Loop:
A `for loop` has 3 statements within it:
1. `let i = 0` - this runs before the loop starts
2. `i < guardian.length` - a conditional statement that check to see if `i` is less then the length of the array
3. `i++` which increases the value of `i` after each iteration of the loop

The declaration block of this loop is the console logging each index of the variable `guardian` based off the value of `i`
```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

for (let i = 0; i < guardians.length; i++) {
    console.log(guardians[i])
    // output:
        // Groot
        // Star Lord
        // Gamora
        // Mantis
}
```

#### ForEach
The `forEach` method operate the same ways as a `for loop`.  runs a provided function once for each array element.


```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']
guardians.forEach(guardian => console.log(guardian))
```