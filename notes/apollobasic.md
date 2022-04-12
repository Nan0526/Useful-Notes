# 快速setup流程  
详细教程：https://odyssey.apollographql.com/lift-off-part1 
1. Define schema
2. Backend - build graphql API with apollo server
3. Frontend - Apollo client

## Schema
A schema is like a contract between the server and the client.   
语言就是SDL `Schema Definition Language`   
A schema is a collection of object types that contain fields.   
如何写schema?   
1. 创建一个js file, 比如 `schema.js`
2. install `apollo-server`. `npm install apollo-server graphql`    
3. import gql
4. 在`gql` template里面定义types..之类的    
```javascript
schema = Schema(query=Query, mutation=Mutation)
```
## Backend: build GraphQL server
Graphql server主要做：    
1. receive graphql query from client
2. validate query against our schema
3. Populate data and return response   
```javascript
const {ApolloServer} = require('apollo-server');
const typeDefs = require('./schema');
const server = new ApolloServer({typeDefs});
```
## Frontend: Apollo Client
We first need to install 2 packages: `graphql` and `@apollo/client`.    
`ApolloClient` is the class that represents Apollo Client itself.   
We will create a new client instance like:   
```javascript
const client = new ApolloClient({
  uri: 'http://localhost:4000',
  cache: new InMemoryCache()
});
```
`ApolloProvider` component uses React's Context API to make a configured Apollo Client instance.    
```javascript
ReactDOM.render(
  <ApolloProvider client={client}>
    <GlobalStyles />
    <Pages />
  </ApolloProvider>,
  document.getElementById('root')
);
```
## Run queries in components   
现在我们的server和client都build好了。 接下来就是在components里面run query然后获得data    
主要有两步：
1. 写query. 用`gql` template来define
2. execute query.  用`useQuery` hook, 这个就比较熟悉了。       

