# Refs
理解：react app是一个DOM tree, 运用Refs可以直接access 到某一个node   
## How to make an input component focused    
就是有一个输入text的Input, 要选中的那样儿    
3步：
1. create a ref using `react.createRef()`    
2. attach this ref to our input element in the render method   
3. call the focus() method
```javascript
import React, { Component } from 'react'

class RefsDemo extends Component {
    constructor(props) {
        super(props)
    
        this.inputRef = React.createRef()
    }

    componentDidMount() {
        {/* this.inputRef.current points to <input/> DOM node */}
        this.inputRef.current.focus()
        console.log(this.inputRef)
    }
    
    render() {
        return (
            <div>
                {/* this.inputRef.current points to <input/> DOM node */}
                 <input type="text" ref={this.inputRef} />
            </div>
        )
    }
}

export default RefsDemo
```
## Refs with Class Components 
我们也可以按照上面的方式在parent component里面attach一个ref到childcomponent里面。 但是注意refs只能在class component里面使用，不能在function component里面用。    
## Forwarding Refs   
Forwarding ref techinique allows the parent component to directly reference the native input element.    
We have 4 simple steps:   
1. Create a ref in the parent component.    
在constructor里面，加上 `this.inputRef = React.createRef()`
2. Attach the ref to the child component using the ref attribute
