# Mutation
To modify data, we need to use another type of GraphQL operation: **mutations**, which are **write operations**    
基本上长这样：
```javascript
type Mutation {
  // 有点像函数名字
  incrementTrackViews(id: ID!): IncrementTrackViewsResponse!  //return的是response type
}
```
复习： 这里的**incrementTrackViews** 并不是function啊，具体的逻辑是由resolver来写。

## Call mutation
To call a mutation, you must use the keyword **mutation** before your GraphQL query.   
```javascript
var query = `mutation CreateMessage($input: MessageInput) {
  createMessage(input: $input) {
    id
  }
}`;
```
然后再在code里面用 `useMutation` 吗？！感觉和 `useQuery`好像
