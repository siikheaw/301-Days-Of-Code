## #005 : Aug 02, 2020
### Today
React Events
### Links
- https://snippets.cacher.io/snippet/d19497a75a516260720e  
- https://snippets.cacher.io/snippet/e0618cc16b70438c8c29

---

# React Events
### Handling Events in React

React wrap events in SyntheticEvent.  

#### Handling event in JavaScript
```js
/* Handling Events in JavaScript */
<button onClick="this.handleClick()">Click</button>
```

#### Handling event in React
```js
/* Handling Events in React */
handleClick() {
  /* ... */
}
<button onClick={this.handleClick}>Click</button> /* no () because we don't want to run when page loaded, but when component mounted. */
```


