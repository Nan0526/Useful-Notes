# Component Lifecycle
1. Life cycle methods only exist in the **class components**, BUT Hook can make this kind of method exist in Functional Components.
2. Mouting, Updating, Unmounting and Error Handling
3. List of functions of cycling methods

# What's is mounting? 
首先要理解mounting是什么
1. 首先要理解，什么是DOM(Document Object Model)
就是HTML的树状结构
```
html
|_ head
|_ body
    |_ id="root"  // <div id="root"></div>
```
在react app的index.js里面   
```
ReactDOM.render(
    <App />,
    document.getElementById('root')
);
```
2. What is Mount and Unmount？
Component is Mounted when it's inserted into the DOM   
当一个component 被mounted，它的其他children component也会被mounted

## Mounting Methods
主要有三个：
这样理解，下面的都是class methods, 是可以在class components里面inherit和override   
1. `constructor()`：
不允许side effects (比如Ajax calls)。可以直接通过 `this.state` 赋值。必须要有`super(props)`
2. `render()`
3. `componentDidMount()`:
Invoked immediately after a component and all its children components have been rendered to the DOM. 允许side effencts，比如ajax calls.    

## Component Updating   
当一个component的state 或者Props变化后，会触发一系列的Update 过程。我在此称之为re-render cycles. 一系列的functions会按照顺序出发：     
1. constructor(props)    
2. static getDerivedStateFromProps(props, state)(很少用到）    
3. render()    
4. getSnapShotBeforeUpdate(prevProps, prevState)(很少用到）    
5. componentDidUpdate(prevProps, prevSate, snapshot)（snapshot是4传下来的）   
在每个re-render cycle只会被call一次，所以我们可以在这里cause side effects, 比如make Ajax calls
