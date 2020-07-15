# Training - Arrays
**Approx. Time:** 45min

## Objective
A Quick synopsis of what will be covered in the training.

## Key Takeaways
A bulleted list of key concepts that students should understand after completion of this training.

* Key Take away 1
* Key Take away 2
* Key Take away 3
* Key Take away 4
* Key Take away 5

## Getting Started
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
2. Set the variable's value to an Array
   - Utilizing the `bracket operator`
3. Set values to the arrays indexes
```js
let array1 = [1, 2, 3]
console.log(array1) // output: (3) [1, 2, 3]
```

### Array Constructor:
The array constructor is the original syntax for instantiating an `Array`. You utilize it by declaring the `new` keyword along with the `Array()` constructor to create a new Array.

```js
let array1 = new Array(1, 2, 3)
console.log(array2) // output: (3) [1, 2, 3]
```

Whereas the `Array constructor` and the `Array literal` perform the same task, yet the `Array constructor` does allots you 1 extra feature.

You are able to instantiate an array with blank indices:

```js
let emptyArray = new Array(3)
console.log(emptyArray) // output: (3) [empty × 3]
```

By convention it is rare to ever use the Array Constructor `new Array()`. The Array literal method is simple, more readably, and has faster execution speed. Stick with that.

## Accessing
You access an Array with the brackets operator `[]`. Each element stored in an array is house in what is called an `index`. We use zero-based indices to access an Array in Javascript, meaning an Array’s first index starts at `0`.

```js
let array 1 = [
    'I am located in index 0',
    'I am located in index 1',
    'I am located in index 2',
]
console.log(array1[0]) // output: I am located in index 0
```

## Changing an Array Element
You are able to change an element value by:
1. Accessing it by its index location within the `Array`
2. Setting that accessed value to the new value

```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

guardians[2] = 'Thor'
```
## Arrays are Objects
Arrays are objects, if you use the `typeof` operator on an Array it returns `"object"`.

```js
let array = []

typeof(array) // Outputs: "object"
```

 `Arrays` are considered a special type of `object` and in turn we describe them as `Arrays`.

## The Length Property
The `length` property counts the total number of indices stored in an array and returns the amount.

```js
let sg1 = ["Teal'c", "Carter", "O'Neill", "Jackson"]
sg1.length //outputs: 4
```
Whereas the index of an Array is accessed using zero-based indices we count the length property with traditional counting methods. ie: `Teal'c` is stored in the first index which is `index 0`

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
}

    // output:
        // Groot
        // Star Lord
        // Gamora
        // Mantis
```

#### ForEach
The `forEach` method operate the same ways as a `for loop` in the sense that it used to iterate over the array to do some kind of work to it.

`forEach` runs a provided function once for each element within the array.

```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

guardians.forEach(guardian => console.log(guardian))
```

Let's break this down:
1. We access the array via the variable it is stored within `guardians`
2. We invoke the method `forEach` on the `guardians` variable
3. For the first argument we provide a function which takes in each guardian's name and console logs it

You could make your code more reusable be doing the following:
```js
let guardians = ['Groot', 'Star Lord', 'Gamora', 'Mantis']

let printNames = (guardianName) => console.log(guardianName)

guardians.forEach(printNames)
```

Note:
- `forEach` always returns the value undefined and is not chainable
- `forEach` does not return a new array



### Filter Method
The `filter method` allows you to perform a function that checks for specific criteria and any element that pass said check is returned in **a new array**
```js
const numbers = [1, 20, 50, 150, 200, 500, 1000]

const results = numbers.filter(number => number < 200)

console.log(results)
```
You could make your code more reusable be doing the following:
```js
const numbers = [1, 20, 50, 150, 200, 500, 1000]

let isNumberLessThan = (number) => number < 200

const results = numbers.filter(isNumberLessThan)

console.log(results)
```

### Reduce Method
The `reduce method` allows you to perform a function which reduces an array to a single value. This method does not change the original array.
```js
let array = [1, 2, 3, 4, 5]

console.log(array.reduce((acc, cur) => {
    console.log(`acc is: ${acc} | cur: ${cur}`)
    return acc * cur
}))
```


You could make your code more reusable be doing the following:

```js
let array = [1, 2, 3, 4, 5]

let reducer = (acc, cur) => acc * cur

console.log(array.reduce(reducer))
```
### Push Method
The `push method` allow you to add as many elements as you would like to an array and returns the new length. This method does affect the original array.

```js
let pokebag = ['pikachu', 'bulbasaur', 'butterfree']

pokebag.push('charizard')
```

## Pop Method

The `pop method` allows you to remove the last element from an array and returns the array. This method does affect the original array.

```js
let avengers = ['Thor', 'Dr. Strange', 'The Hulk', 'Caption Marvel', 'Iron Man']

avengers.pop()
```