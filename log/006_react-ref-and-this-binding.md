




# React Refs and this Binding
### this Binding
The Golden Rule in React is **DON'T Touch The DOM.**

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
