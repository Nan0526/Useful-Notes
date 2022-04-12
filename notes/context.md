# Context 
Context provides a way to pass data through the component tree without having to pass props down manually at every level.   

## Context API
1. Create the context
2. Provide a context value
3. Consume the context value 

### Create the context
一个新file `userContext.js`   
```
import React from 'react'

const UserContext = React.createContext()

const UserProvider = UserContext.Provider
const UserConsumer = UserContext.Consumer

export { UserProvider, UserConsumer }
```
### Provide a context value
在App node里面：
```
...
<UserProvider value="abc">
  <ChildComponent />
</UserProvider>
...
```
### Consume the context value
在child component里面，consume context value:
```
<UserConsumer>
 {
  (username) => {
    return <div>Hello {username}</div>
  }
 }
</UserConsumer>
```
