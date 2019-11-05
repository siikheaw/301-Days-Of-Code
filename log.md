# #301DaysOfCode - Log
The daily log of my **#301DaysOfCode** challenge.

## Log

### Day 1: October 26, 2019
**Today:**  
Create an element in [amp library].

**Link:**  
[amp - Buttons](https://codepen.io/siikheaw/pen/JjjJPza)

### Day 2: October 27, 2019
**Today:**  
Create an element in [amp library].

**Link:**
[amp - Cards](https://codepen.io/siikheaw/pen/yLLXbQg)

### Day 3: October 28, 2019
**Today:**  
Create an element in [amp library].

**Link:**  
[amp-Rolling text](https://codepen.io/siikheaw/pen/KKKqRQJ)

### Day 4: October 29, 2019
**Today:**  
Create an element in [amp library].

**Link:**  
[amp-Button with icon](https://codepen.io/siikheaw/pen/zYYzVbe)

### Day 5: October 30, 2019
**Today:**  
Create an element in [amp library].

**Link:**  
[amp-Media object](https://codepen.io/siikheaw/pen/WNNEgGd)

### Day 6: October 31, 2019
**Today:**  
Create an element in [amp library].

**Link:**  
[amp-Another cards](https://codepen.io/siikheaw/pen/WNNXGMZ)

### Day 7: November 1, 2019
**Today:**  
A tutorial in JavaScript30: JS Drum Kit.

**Link:**
[JS Drum Kit](https://codepen.io/siikheaw/pen/BaaYeRp)

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

### Day 8: November 2, 2019
**Today:**  
A tutorial in JavaScript30: JS + CSS Clock.

**Link:**  
[JS + CSS Clock](https://codepen.io/siikheaw/pen/ExxQzbM?editors=0110)

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
  
### Day 9: November 5, 2019
**Today:**  
A tutorial in JavaScript30: CSS Variables & JS.

**Link:**  
[CSS Vars & JS](https://codepen.io/siikheaw/pen/vYYRBvK)

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

- Set the CSS properties with setProperties.
  ```js
  document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
  ```







