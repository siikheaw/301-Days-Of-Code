## #005 : Aug 02, 2020
### Today
React Refs and this Binding
### Links


---

# React Refs and this Binding

The Golden Rule in React is **DON'T Touch The DOM.**
Example: How can we select the 'input' in form element.
```js
<form className="store-selector" onSubmit={this.gotoStore}>
  <input
    type="text"
    defaultValue={getFunName()}
  />
  <button type="submit">Visit Store</button>
</form>
```

DON'T do this in React.
```js
/* Don't touch the DOM */
const storeName = document.querySelector('input'); // vanilla
/* or */
const storeName = $('input'); // jQuery
```

Instead, use Refs or State.
```js
myInput = React.createRef(); // create empty Ref
  /* ... some code ... */
<form className="store-selector" onSubmit={this.gotoStore}>
  <input
    type="text"
    ref={this.myInput}
    defaultValue={getFunName()}
  />
  <button type="submit">Visit Store</button>
</form>
```

## Binding this
By default, 'this' bound with build-in method like render, but not bound with our own component. 
```js
myInput = React.createRef();
goToStore(event) =  {
  console.log(this); // -> undefined
}
```

So we need to munually bind 'this'
```js
/* bind this to our own component */
constructor() {
  super();
  this.goToStore = this.goToStore.bind(this);
}
goToStore(event) =  {
  console.log(this); // -> our component
}
```

Anyway, the easiest way is to use the arrow function.
```js
goToStore = event => {
  console.log(this); // -> our component
}
```

See the full code in the link above.
