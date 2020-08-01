### Day 3: August 1, 2020
**Today** - React Stateless Functional Component, more on props  
**Link**  - https://snippets.cacher.io/snippet/be73c1c97bc54d032469

### Stateless Functional Components
If the component only has a 'render' (and props) method, can turn that component to Stateless component.
```js
function Header (props) {
    return (
        <span>{props.tagline}</span>
    )
}

/* or using arrow function */
const Header (props) => {
    return (
         <span>{props.tagline}</span>
    )
}

/* more on props */
const Header ({ tagline, age }) => {
    return (
        <span>{tagline} {age}</span> /* App.js - <Header tagline="Show Me Money" age="21" /> */
    )
}
