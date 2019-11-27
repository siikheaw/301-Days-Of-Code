- Create copied array from something.
  ```js
  const keys = Array.from(document.querySelectorAll('.key'));
  ```
- Do something with each array items with ``forEach``.
  ```js
  keys.forEach(key => key.addEventListener('transitionend', removeTransition));
  ```

---

## Array methods

### `filter`   
Use filter if you already have an array, and you want to grab certain values that match a criteria from that array — e.g., even numbers, words longer than 10 characters, etc.  
```js
// 1. Filter the list of inventors for those who were born in the 1500's
// ------------------------------------------------------------------------
const fifteen = inventors.filter(inventor => (inventor.year > 1500 && inventor.year < 1600));
```
### `map`
Use map if you already have an array, and you want to perform the same action on every element in the array and return the same number of elements in a new array.
```js
// 2. Give us an array of the inventors' first and last names
// ------------------------------------------------------------------------
const fullName = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
```
### `sort`
```js
// 3. Sort the inventors by birthdate, oldest to youngest
// ------------------------------------------------------------------------
const ordered = inventors.sort((a, b) => (a.year > b.year) ? 1 : -1);
```

### `reduce`  
Use reduce if you already have an array, but you want to use the values in that array to create something new.
```js
const totalYears = inventors.reduce(function(total, inventor) {
  return total + (inventor.passed - inventor.year);
}, 0)
```



[JavaScript — Filter, Map, Reduce](https://medium.com/better-programming/javascript-filter-map-reduce-9ab7fbe6f193)  
Use filter if you already have an array, and you want to grab certain values that match a criteria from that array — e.g., even numbers, words longer than 10 characters, etc.
Use map if you already have an array, and you want to perform the same action on every element in the array and return the same number of elements in a new array.
Use reduce if you already have an array, but you want to use the values in that array to create something new.

---

### `some()`
  ```js
  // Array.prototype.some()  
  // is at least one person 19 or older?  
  const isAdult = people.some(person => ((new Date()).getFullYear() - person.year >= 19));
  ```
### `every()`
  ```js
  // Array.prototype.every()  
  // is everyone 19 or older?  
  const allAdults = people.every(person => ((new Date().getFullYear())) - person.year >= 19);
  ```
### `find()`
  ```js
  // Find is like filter, but instead returns just the one you are looking for  
  // find the comment with the ID of 823423
  const comment = comments.find(comment => comment.id === 823423);
  ```
### `findIndex()`
  ```js
  // Find the comment with this ID
  // delete the comment with the ID of 823423
  const index = comments.findIndex(comment => comment.id === 823423);
  console.log(index);
  comments.splice(index, 1);
  console.log(comments);
  ```

---

## Destructing array
```js
[lastX, lastY] = [e.offsetX, e.offsetY];
```
