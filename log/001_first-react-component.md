### Day 1: July 30, 2020
**Today** - First React component.  
**Link**  - https://codesandbox.io/s/wesbos-react-beginner-6f01w?file=/src/components/StorePicker.js  

```js
/*  React Boilerplate
    index.js */
import React from 'react';
import { render } from 'react-dom'; // import only render method from react-dom
import StorePicker from './components/StorePicker'; // import StorePicker component

render (<Storepicker />, document.querySelector('#root'); // (what to render, where to render)

/*  Components
    StorePicker.js */
import React from 'react';
class StorePicker extends React.Component {
  render() {
    return <p>Hello World!</p>
  }
}
export default StorePicker
```
