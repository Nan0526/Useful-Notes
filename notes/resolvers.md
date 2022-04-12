## Journey of a graphql query
https://odyssey.apollographql.com/lift-off-part2/querying-live-data 这个教程里的resolvers都是用js写的
1. Client side: create a query. Then shape the query as a string. Then it sends the query to the server in an HTTP POST or GET request.
2. Serverside: 
    1. 接收query 
    2. parse query 
    3. validate query/types against schema 
    4. For each field in the query, the server invokes that field's **resolver function**.    
    每一个field都有一个resolver function. Resolver function的作用是 ‘resolve’ its field by pupulating it with the correct data from the correct source, such as a DB or a REST API. 
    5. 返回data给client

## Resolver
Resolver可以从各个data source获得数据，DB, API...    
A resolver is a function. It has the **same name as the field** that it populates data for.    
