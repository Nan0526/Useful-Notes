# Pure Component
在此之前要先懂component mounting和component updating的life cycle!    
A PureComponent implements the `shouldComponentUpdate` lifecycle method by performing a shallow comparison on the props and state of the component.    
If there is no difference, the component is not re-redered - performance boost.   
就是，它会比较（浅比较）之前和现在的props和state. 如果没区别的话，就不会re-render. 注意的是永远不要mutate state, 要return a new object!   
```javascript
import React, { PureComponent } from `react`

class PureComp extends PureComponent {
  render() {
    return (
      <div>
        Pure Component
      </div>
    )
  }
}
```
