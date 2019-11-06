---
id: structure
title: Structure
sidebar_label: Structure
---
<br><br>
Let's start by structuring our App.
First we will need to add the [__Router__](router.md) component to handle all the different paths. And for each path we will want a [__Route__](route.md) component. 

![Routing](/docs/assets/firsttutorial_routing1.gif)

> You can delete the default children of each created component.

Now we configure each [__Route__](route.md) component. On the __component settings__ tab we set the `Label`, `Path` and `Default path` settings for each of them:

| Label       | Path                | Default Path     |
|-------------|---------------------|------------------|
| Home        | /                   |                  |
| Message     | /message/:messageid | /message/default |
| PostMessage | /newMessage         |                  |

> We will be using the messageid as a parameter to fetch and show each individual message.

![Routing](/docs/assets/firsttutorial_routing2.gif)

Starting with the __Home Route__ we will add a [__Query__](query.md) component to get the data from our Graphql DB endpoint. Then to it we add a [__ReplicateList__](replicatelist.md) which will ease our job by replicating, with the help of it's parent, each instance of data (__Message__) received. 
<br><br>
For each __Message__ we will want to show its __Title__ (which will be a link to the individual message) and __Date__, so we add the following components:

![Home](/docs/assets/firsttutorial_home.png)

For the __Message Route__ we will want also a [__Query__](query.md) component to fetch our __Message__ and each component to display its previous data and the __Description__ aswell:

![Message](/docs/assets/firsttutorial_message.png)

At last the __PostMessage Route__ as our form to submit new Messages, will have a [__State__](state.md) component with a child [__Form__](form.md) and 
this will have the following components for input:

![PostMessage](/docs/assets/firsttutorial_postmessage.png)

So to wrap our structure, this is all we will need.
<br><br><br>
