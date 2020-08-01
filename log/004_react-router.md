## Day 4: Aug 02, 2020
**Today** - React Router  
**Link** - https://snippets.cacher.io/snippet/4d547101818c7497447f  

> React Router is the de facto standard routing library for React. When you need to navigate through a React application with multiple views, you’ll need a router to manage the URLs. React Router takes care of that, keeping your application UI and the URL in sync.  
[React Router v5: The Complete Guide](https://www.sitepoint.com/react-router-complete-guide/)

```js
/* Router.js */
const Router = () => (
  <BrowserRouter>
    <Switch>
      <Route exact path="/" component={StorePicker} /> /* When the route is exact '/', render the 'StorePicker' component */
      <Router path="/store/:storeId" component={App} /> /* When the route is 'xx/store/xx', render the 'App' component */
      <Router component={NotFound} /> /* When no match, render the 'NotFound' component */
    </Switch>
  </BrowserRouter>
)
```
