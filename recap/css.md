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