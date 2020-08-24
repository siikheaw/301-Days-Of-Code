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

/* bind this to our own component */
constructor() {
  super();
  this.goToStore = this.goToStore.bind(this); // by default, 'this' not bound with our own component, so we need to munually bind 'this' or using arrow function instead */
}

/* easiest way to bind 'this' is to use arrow function */
goToStore = event => {

}

<form className="store-selector" onSubmit={this.gotoStore}>
  <input
    type="text"
    ref={this.myInput}
    defaultValue={getFunName()}
  />
  <button type="submit">Visit Store</button>
</form>
```

```js
class StorePicker extends React.Component {
  // [2] to bind 'this' use constructor
  // [3] the easier way is to use Arrow Function
  constructor() {
    super();
    this.goToStore = this.goToStore.bind(this);
  }
  myInput = React.createRef(); /* Create Ref */
  
  goToStore(event) { /* Our method not bind to React.Component by default, so 'this' is not refer to this component */
    event.preventDefalt();
    
    // get the text from that input
    // this is wrong, DON'T touch the DOM
    const storeName = $('input');
    // Instead, use the refs or state
    // Anyway, we have some problem with 'this'
    // [1]'this' in method is undefined
    console.log(this); /* -> (this) undefined */
  }
  
    // [3] use Arrow function to bind 'this' to an instance
    goToStore = (event) => {
      console.log(this); // -> StorePicker
    }
    
  
  render () {
    // [1] 'this' in render is ref to the component
    console.log(this); /* StorePicker */
    return (
      <form onSubmit={this.goToStore}>
        <input type="text" ref={this.myInput} defaultValue={getFunName()} />
        <button type="submit">Visit Store</button>
      </form>
    );
  }
}
```
