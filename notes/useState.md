# useState
- The useState hook lets you add state to functional components
- In classes, the state is always an object
- With the useSate hook, the satte doesn't have to be an object
- The useState hook returns an array with 2 elements. The first element is the current value of the state, and the second element is a state setter function.     
________
revisit创建一个counter的三步：1.需要一个component 2.需要一个state value 3.需要一个Method来改变这个state value     
useState 直接实现后两步
```javascript
const [count, setCount] = useState(0)
```
完整版component:
```javascript
import React, {useState} from `react`

function HookCounter() {
 const [count, setCount] = useState(0)
 return (
    <div>
      <button onClick={() => setCount(count+1)}>Count {count}</button>
    </div>
 )
}
```
# useState with previous state
其实上一个例子并不是最安全的方法，如果我们想update state value based on previous state value的话。最好的办法并不是 `setCount(count + 1)` 而是 `setCount(prevCount => prevCount + 1)`

# useState with Object
当state是一个object的时候， 比如 `const [name, setName] = useState({'firstName': '', 'lastName': ''})`. update其中的一个property要注意，useState不会automerge. 比如：   
```javascript
setName({'firstName': 'hello'})
``` 
就直接把`lastName` property 搞没了。   
正确的做法是：   
```javascript
setName(...name, {'firstName': 'hello'})
``` 

# useState with Array
array 和 object一样，update的时候都不会automerge, 所以也要先做一个copy.
```javascript
const [items, setItems] = useState([])
const addItem = () => {
   setItems([...items, //...items 是make a copy
   { 
      id: items.length,
      value: Math.floor(Math.random() * 10) + 1
   }])
}
```
