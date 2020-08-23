# ⚛️ React

React is a JavaScript library for building user interfaces.<sup>[1](#react)</sup>

## A Simple Component
React components implement a render() method that takes input data and returns what to display. This example uses an XML-like syntax called JSX. Input data that is passed into the component can be accessed by render() via this.props.<sup>[1](#react)</sup>

JSX is optional and not required to use React.

## A Stateful Component
In addition to taking input data (accessed via this.props), a component can maintain internal state data (accessed via this.state). When a component’s state data changes, the rendered markup will be updated by re-invoking render().<sup>[1](#react)</sup>

## An Application
Using props and state, we can put together a small Todo application. This example uses state to track the current list of items as well as the text that the user has entered. Although event handlers appear to be rendered inline, they will be collected and implemented using event delegation.<sup>[1](#react)</sup>

---

## Components
Everything in react is component.<sup>[2](#wesbos)</sup>




---
## References
<a name="react">1</a>: https://reactjs.org/
<a name="wesbos">2</a>: xxx
