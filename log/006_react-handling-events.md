## #006 August 03, 2020
### React Handling Events
- https://snippets.cacher.io/snippet/ea1ca973a86773f2f7e0

---

```js
/* StorePicker.js */
/* ... */
  goToStore = event => {
    // 1. Stop the form from submitting
    event.preventDefault();
    // 2. get the text from that input
    const storeName = this.myInput.value.value;
    // 3. Change the page to /store/whatever-they-entered
    this.history.props.push(`/store/${storeName}`); /* Not reloading the page, just change the page-url with Router /
  }
/* ... */
```
