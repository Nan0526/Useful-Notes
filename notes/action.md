# Actions
Plain JavaScript objects    
Must have a 'type' property     
```javascript
const BUY_CAKE = 'BUT_CAKE'
/* action */
{
  type: BUY_CAKE,
  into: 'first redux action'
}
/* action creator */
function buyCake() {
  return {
    type: BUY_CAKE,
    into: 'first redux action'
}
}
```
