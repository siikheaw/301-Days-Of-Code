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
**Link:**   
**Digest:**  

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
