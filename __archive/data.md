---
id: data
title: Data
sidebar_label: Data
---
<br><br>
Someone at the back-end will have to take care of the DB. Well, we can be that someone.

For this tutorial we will use the __GraphCool__ interface: [__Graph.cool__](https://www.graph.cool)

Open Graphcool console and set up a new project with the following `Type`:

```
type Message @model {
  date: DateTime!
  description: String!
  id: ID! @isUnique
  title: String!
}
```

Grab the endpoint url so we can set it up in our App. 
<br>
Back to __Shift__ we go to the __Code__ tab and insert the url endpoint into the __GraphQL Settings__<br>(`Code->Settings->GraphQL`)

Our connection is ready. Now we need two [__Queries__](queries.md) and one [__Mutation__](mutations.md):

- query __allMessages__ - all the messages to be shown in the Messages feed.
- query __message__ - the individual message fetched using it's `id`.
- mutation __postMessage__ - post messages.

>In __Code Mode__ you can not only add this queries and mutation but also use the [__GraphiQL__](https://github.com/graphql/graphiql) interface to do it. All this inside __Shift__.

```
query allMessages {
  allMessages {
    id
    title
    description
    date
  }
}
```

```
query message ($id: ID!) {
  Message (id: $id){
    id
    title
    description
    date
  }
}
```

```
mutation addMessage (
	$description: String!
	$date: DateTime!
	$title: String!){
    createMessage(
      description: $description
      date: $date
      title: $title) {
			id
            title
            description
            date
    }
  }
```

> Each __Query__ and __Mutation__ needs to be added separately 

Another step complete, it's time to create data.
<br><br><br>
