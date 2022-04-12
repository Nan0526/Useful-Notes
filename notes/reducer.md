# Reducer 
本质是一个function! input:prevSate, action. output: nextState    
```
(previousSate, action) => newState
```
例子：   
```
const initialState = {
  numOfCakes: 10
}

const reducer = (state=initialSate, action) => {
  switch(action.type) =>{
    case BUY_CAKE: return {
      ...state, /* 注意这个省略号+Object的用法！*/
      numOfCakes: state.numOfCakes - 1,
    }
    default: return state
  }
}
```
