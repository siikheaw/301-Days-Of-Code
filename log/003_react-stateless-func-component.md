

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
