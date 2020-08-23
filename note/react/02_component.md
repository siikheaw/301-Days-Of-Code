# Component
Everything in React is component.

## Basic Structure
```js
import React from 'react';
import { render } from 'react-dom';

class MyComponent extends React.Component {
  render () {
    return (
      { /* jsx code here */}
    )
  }
}

export default MyComponent;
```

or
```js
import { Component } from 'react';
import { render } from 'react-dom';

class MyComponent extends Component {
  render () {
    return (
      { /* jsx code here */}
    )
  }
}

export default MyComponent;
```

Then bundle all component into the main file.
```js
import { Component } from 'react';
import { render } from 'react-dom';
import MyComponent from './components/MyComponent';
import './css/style.css';

render(<MyComponent />, document.querySelector('#main'));
```
