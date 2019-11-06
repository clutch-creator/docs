---
id: graphql
title: GraphQL
sidebar_label: GraphQL
---

`"GraphQL is a query language for your API, and a server-side runtime for executing queries by using a type system you define for your data. GraphQL isn't tied to any specific database or storage engine and is instead backed by your existing code and data."`


In the older days in order to fetch data from a database you would need to be a database query expert and run complex queries. With __Graphql__ it gets not only simpler to write a query for the information you want but it also just gives you specific information without delivering a gigantic response where half the data is not used.

## Queries, Mutations and Subscriptions

((How to address this in a simple way for basics without copying graphql entire documentation ))
### Queries

### Mutations

### Subscriptions


### Queries as Components

After each Query, Mutation and Subscription creation, these become available to use as [__Components__](components.md) in the [__Builder__](builder.md) meaning you can easily use them for data presentation, mutation or subscription with simple configuration reusing their code.

Please refer to our walkthrough of how to use [__Queries as Components__](queries-as-components.md) in the __Walkthrough__ section.


## GraphiQL

The well-known graphical interactive in-browser GraphQL IDE is implemented in __Shift__ and it helps on every query manipulation by not only delivering documentation for each Query Type but with a set of features like: 
* Syntax highlighting
* Intelligent type ahead of fields, arguments, types, and more.
* Real-time error highlighting and reporting.
* Automatic query completion.
* Run and inspect query results.

A useful playground to implement, test and run your queries.


## Shift Dummy GraphQL & GraphiQL

In the occasion of not having an already configured, apopulated database, a GraphQL endpoint for it or even for testing purposes, __Shift__ provides a _Dummy_ server of either GraphQL and GraphiQL instances for quick test, mock and implementation. These can be accessed at:

* Dummy Graphql Endpoint - ############# 
* Dummy Graphiql Endpoint - ############# 

## Debugging
With the help of the GraphiQL interface it is easier to debug your query building.

### Documentation
Documentation is one of the focus points of GraphQL, and GraphiQL uses it. It can be accesible inside GraphiQL and it is possible to explore queries, mutations, fields, their types, if they’re required, etc. Even if your server has not been documented with descriptions, there is always the graph structure that will be of great help.

__Explore the Documentation Explorer:__
* In the __GraphiQL__ interface select the top right button __Docs__
* It will open the __Documentation explorer__
* Use the search textfield to search through the documentation

### Utilities
GraphiQL also provides the following useful debugging features:
* __Debugging as-you-type__ - highlighting errors and providing intelligent type for auto-completion and hints
* __Json Viewer__ - a read-only, copy support, code folding with automatic identation viewer for response display
* __Variables pane__ - Stores your current variable use under the selected query

And don't forget the most useful key shortcut __Shift__ + __Space__ which will list all the fields the current schema supports.

## Subscriptions

((This is for advanced))

## References

* __GraphiQL Github__ - [github.com](https://github.com/graphql/graphiql)
* __GraphQL__ - [graphql.org/](http://graphql.org/learn/)
