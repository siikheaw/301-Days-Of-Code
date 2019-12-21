### Day 7: November 1, 2019
**Today:** A tutorial in JavaScript30: JS Drum Kit.  
**Link:** [JS Drum Kit](https://codepen.io/siikheaw/pen/BaaYeRp)  
**Digest:**  
- Create copied array from something.
  ```js
  const keys = Array.from(document.querySelectorAll('.key'));
  ```
- Do something with each array items with ``forEach``.
  ```js
  keys.forEach(key => key.addEventListener('transitionend', removeTransition));
  ```
- Select the elements with CSS properties.
  ```js
  if (e.propertyName !== 'transform') return; // detect only 'transform' property
  ```
- Add & Remove CSS classes.
  ```js
  key.classList.add('playing');
  ```
  ```js
  e.target.classList.remove('playing');
  ```

---

### Day 8: November 2, 2019
**Today:** A tutorial in JavaScript30: JS + CSS Clock.  
**Link:** [JS + CSS Clock](https://codepen.io/siikheaw/pen/ExxQzbM?editors=0110)  
**Digest:**  
- Get the current time using ``new Date()``.  
  ```js
  const now = new Date();
  const seconds = now.getSeconds();
  const mins = now.getMinutes();
  const hours = now.getHours();
  ```
- Insert CSS styles from JS using ``style.property``
  ```js
  const secondsDegrees = ((seconds / 60) * 360) + 90;
  secondHand.style.transform = `rotate(${secondsDegrees}deg)`;
  ```
---

### Day 9: November 5, 2019
**Today:** A tutorial in JavaScript30: CSS Variables & JS.  
**Link:** [CSS Vars & JS](https://codepen.io/siikheaw/pen/vYYRBvK)  
**Digest:**  
- CSS variables.
  ```css
  :root { --spacing: 10px; }
  .h1 { padding: var(--spacing); // 10px
  ```

- HTML ``data-*``
  ```html
  <input id="spacing" type="range" name="spacing" min="10" max="200" value="10" data-sizing="px">
  ```

- Get the elements with dataset
  ```js
  const suffix = this.dataset.sizing || ''; // dataset = object contains data-*
  ```

- Set the CSS properties with setProperty.
  ```js
  document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
  ```

---
  
### Day 10: November 6, 2019
**Today:** A tutorial in JavaScript30: Array Cardio Day 1  
**Link:** [Array Cardio Day 1](https://codepen.io/siikheaw/pen/wvvYeov)  
**Digest:**  
  [Filter, Map, Reduce](https://medium.com/better-programming/javascript-filter-map-reduce-9ab7fbe6f193)  
- filter  
Use filter if you already have an array, and you want to grab certain values that match a criteria from that array — e.g., even numbers, words longer than 10 characters, etc.  
  ```js
  // 1. Filter the list of inventors for those who were born in the 1500's
  // ------------------------------------------------------------------------
  const fifteen = inventors.filter(inventor => (inventor.year > 1500 && inventor.year < 1600));
  ```
- map  
Use map if you already have an array, and you want to perform the same action on every element in the array and return the same number of elements in a new array.
  ```js
  // 2. Give us an array of the inventors' first and last names
  // ------------------------------------------------------------------------
  const fullName = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
  ```
- sort  
  ```js
  // 3. Sort the inventors by birthdate, oldest to youngest
  // ------------------------------------------------------------------------
  const ordered = inventors.sort((a, b) => (a.year > b.year) ? 1 : -1);
  ```
- reduce  
Use reduce if you already have an array, but you want to use the values in that array to create something new.
  ```js
  const totalYears = inventors.reduce(function(total, inventor) {
    return total + (inventor.passed - inventor.year);
  }, 0)
  ```

---

### Day 11: November 7, 2019
**Today:** A tutorial in JavaScript30: Flex Panels Image Gallery  
**Link:** [Flex Panels Image Gallery](https://codepen.io/siikheaw/pen/BaaxRKN?editors=0110)  
**Digest:**  
- Using Nested Flexbox.
- Select every x-child.
  ```css
  .panel > *:first-child { transform: translateY(-100%); }
  .panel > *:last-child { transform: translateY(100%); }
  ```
- Loop through every single element using ``forEach``.
  ```js
  const panels = document.querySelectorAll('.panel');
  panels.forEach(panel => panel.addEventListener('click', toggleOpen));
  panels.forEach(panel => panel.addEventListener('transitionend', toggleActive));
  ```
- Toggle classes.
  ```js
  function toggleOpen() {
    this.classList.toggle('open');
  }
  ```
- Select element that ``includes`` specific CSS property.
  ```js
  function toggleActive(e) {
    if (e.propertyName.includes('flex')) {
      this.classList.toggle('open-active');
    }
  }
  ```

---

### Day 12: November 14, 2019
**Today:** A tutorial in JavaScript30: Ajax Type Ahead  
**Link:** [Ajax Type Ahead](https://codepen.io/siikheaw/pen/wvvEwyL)  
**Digest:**  
- fetch
- filter, map
- replace
- RegExp

---

### Day 13: November 15, 2019
**Today:** A tutorial in JavaScript30: Array Cardio Day 2
**Link:** [Array Cardio Day 2](https://codepen.io/siikheaw/pen/mddadRG)  
**Digest:**  
- some
  ```js
  // Array.prototype.some() // is at least one person 19 or older?
  const isAdult = people.some(person => ((new Date()).getFullYear() - person.year >= 19));
  ```
  - every
  ```js
  // Array.prototype.every() // is everyone 19 or older?
  const allAdults = people.every(person => ((new Date().getFullYear())) - person.year >= 19);
  ```
- find
  ```js
  // Find is like filter, but instead returns just the one you are looking for
  // find the comment with the ID of 823423
  const comment = comments.find(comment => comment.id === 823423);
  ```
- findIndex
  ```js
  // Find the comment with this ID
  // delete the comment with the ID of 823423
  const index = comments.findIndex(comment => comment.id === 823423);
  console.log(index);
  comments.splice(index, 1);
  console.log(comments);
  ```

