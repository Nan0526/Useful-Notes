# useReducer
useReducer is a hook that is used for state management.    
It's an alternative to `useState`.     
`useState`本身会用到`useReducer`, 所以`useReducer`是一个更加Primitive hook.    
### Reduce vs useReducer  
我们可以看一下JS里面的`Array.reduce()` method: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce      
*卧槽！我忽然觉得好绕。* `reducer()` 和 `reducer function`是两个不同的东西！！reducer funtion是要传入到 `reducer()`里面的。  

<img width="426" alt="reduce vs usereducer" src="https://user-images.githubusercontent.com/36396754/135365878-08469ba1-99e6-4de6-b2cf-cdfc8c98a8ef.png">
<img width="787" alt="useReducersummary" src="https://user-images.githubusercontent.com/36396754/135366056-c9ba6f76-5cd1-4490-a9f8-16d468fcb782.png">
