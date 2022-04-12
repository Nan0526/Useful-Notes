# Memo 
PureComponent only works in Clase Component! 那么function component用什么呢？主需要在export那里加上：   
```javascript
...
export default React.memo(XXX);
```
