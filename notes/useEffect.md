# useEffect 
The Effect hook lets you perform side effects in functional components   
It's a close replacement for componentDidMount, componentDidUpdate and componentWillUnmount.   
## useEffect after render
userEffect 在每个component的render都会被fire!!(init render + re-render）(就是componentDidMount 和 componentDidUpdate）    
```javascript
useEffect(() => {
  document.title = `You clicked ${count} times`
})
```
### Conditionally run effects   
我们知道state 和prop改变的时候component都会render一次，那useEffect就会不断的被fire，即使不相干。所以这里引入了conditional run:    
```javascript
const [count, setCount] = useState(0)
useEffect(() => {
  document.title = `You clicked ${count} times`
}, [count])
```   
只有state里的count改变的时候，这个useEffect才会Run    
如果用empty array的话，只会被fire一次    
