# Redux
"Redux is a predictable state container for JavaScript apps"

### It is for JavaScript apps   
不是react特有的！react-redux是一个包，可以用来连接react和redux。
### It is a state container   
Redux stores the state of your application. State of an app is the state represented by all the individual components of that app. Redux will store and manage the application state. 
我们之前学过了在react里面的 *component state*, Redux是管理*app state* 比如：   
```
Application
state = {
   isUserLoggedIn: true,
   username: 'Vishwas'
   ...
}
```
### Redux is predictable
In redux, all state transitions are explicit and it is possible to keep track of them.   
The changes to your application's state become predictable   

## Three Core concepts: store, action and reducer
*"The state of your whole application is store in an object tree within a single store"*    
整个app的state是存在一个树状结构里面！   
```
{
   numCakes: 10
}
```
*“The only way to chane the state is to emit an action, an object describing what happened”*    
🙅🏻‍♀️ 不能直接改app的state!需要dispatch 一个action!
```
{
   type: BUY_CAKE
}
```
*"To specify how the state tree is transformed by actions, you write pure reducers"*    
Reducers就是pure functions! `Reducer - (previousState, action) => newState`   
```javascript
const reducer = (state, ction) => {
   switch (action.type) {
      case BUY_CAKE: return {
         numOfCakes: sate.numOfCakes - 1
      }
   }
}
```
