# Tapping into `componentWillUpdate()`
 Once we have determined that we do need to re-render in our Update phase, the `componentWillUpdate()` will be called. The method is passed in two arguments: `nextProps` and `nextState`. The method `componentWillUpdate()` is [similar to `componentWillMount()`](../birth/premounting_with_componentwillmount.md). The difference being that `componentWillUpdate()` is called every time a re-render is required and we get access to the next props and state.
 
 Just like `componentWillMount()`, this method is called before `render()`. Because we have not rendered yet, our Component the Native UI (DOM, etc.) will reflect the old rendered UI. Unlike, `componentWillMount()` we can technically access `refs` but it is not recommended.

The `componentWillUpdate()` is a chance for us to handle configuration, update our state, and in general prepare for the next render. If we want to access the old props or state, we can call `this.props` or `this.state`. We can then compare them to the new values and make changes/calculations as required.
 
 