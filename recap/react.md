# React




---

## Using State Correctly
There are three things you should know about setState().

### 1. Do Not Modify State Directly
```js
// Wrong
this.state.comment = 'Hello';

// Correct
this.setState({comment: 'Hello'});
```
The only place where you can assign this.state is the constructor.

### 2. State Updates May Be Asynchronous
```js
// Wrong
this.setState({
  counter: this.state.counter + this.props.increment,
});

// Correct
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));
```

### 3. State Updates are Merged
When you call setState(), React merges the object you provide into the current state.


---

## Handling Events
- React events are named using camelCase, rather than lowercase.  
- With JSX you pass a function as the event handler, rather than a string.  
- cannot return false to prevent default behavior in React. You must call preventDefault explicitly.  
- 

```js
// HTML
<button onclick="activateLasers()">
  Activate Lasers
</button>

// React
<button onClick={activateLasers}>
  Activate Lasers
</button>
```





