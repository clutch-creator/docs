---
id: content
title: Content
sidebar_label: Content
---
<br><br>
Our app runs on data, receives and submits __Messages__, so let's link it all together. <br>
In Shift's GraphQL interface we are going to "manually" submit messages so we can link data to it's desired place.
<br> (`Code->Settings->GraphQL`) 

In our previously created `addMessage` mutation we will insert messages. At the bottom in `Query Variables` in a json format
we add:

```
{
  "title": "A Pretty Message Title",
  "description": "a random description",
  "date": "2018-05-03"
}
```
> In a first instance we insert the date for the messages submitted manually, but later on this will be done automatically by our app.

From just hitting the play button at the top of the GraphiQL interface we can see that our Mutation query went through and have the
returning information aswell as the id generated for our message.

Now we have messages in our DB, it's time to see it.

### Home

Back in __Designer Mode__, we go to the Route we created as __Home__ and select the previously created __Query__ component. On the
configuration of the __Query__ we set the `Query` option to __allMessages__ (our `Query` defined in Code Mode).

In __ReplicateList's__ child, set the Configuration option `Item Name` to __message__, this will define how we reference each data item.
Set `Each Item Key` to __message.id__ so it uses the message id as key for each data item. Then in __Props Flow__ tab select the __allMessages__ query and `Add new link` with `Data` type, this will bind allMessages received to this __ReplicateList__.

Now to set each message title and date to each righteous place we select the __Text__ child of __ReplicateList__ and in the PropsFlow tab we
bind it to `__message__ -> __title__` and select the `Link` type to Content. Do the same for the __Date__ child but don't forget to set the `Link` type to __Date__.

Till this step, every change you've done to your app had the proper visual update in __Canvas__, it's a good practice to take advantage of this Shift's feature to debug everything that's happening in real-time.

In our plan there was a link that would take us to each individual message, and since we forgot to add it on purpose, let's see how to quickly shortcut and deal with it in Shift.

We add a __Link__ component as child of the __ReplicateList__ and then we drag the __Text__ component (which is our message title) into the  it. In __Link__ Configuration set the `Link` option to __/message/${props.message.id}__. This will set the link path to our __Message__ Route with the message `id` from the __message__ previously received from the __Query__ and fed from the __ReplicateList__.

>As you have noticed the Component-Tree works with Components and Html elements respecting the order of the well known DOM Tree. That's why the __Link__ is added as a parent of __Text__ and not the other way around.


### Message

Since we are routing every message by its `id` as a parameter defined in this __Message__ route (`/message/:messageid`), set a messageid default path in configuration. With the default message set it's now easier to connect all the data to each field.

We need to tell our __Query__ to deal with it.

In __Query__ configuration set the `Query` option as __message__ and the `Arguments` as:

```
{
    id: props.flowProps.route.params.messageid
}
```

"__Query__ deal with it !" we said.

Then just select each field for __title__, __description__ and __date__ and bind them in __Props Flow__ tab like we did before.

>__Tip:__ go to the __Home__ Route and start the preview, see how each link takes you to each individual message path and presentation.

We are done here. How quick was it?

### PostMessage

For the __PostMessage__ Route we will need to configure the __Local State__ component, and __Actions__ for it.

In our __Local State__ component in __State Settings__ tab we set the default state:

```
{
  title: "",
  description: ""
}
```

And add two new __Actions__:


Name: changeField
Template: Synchronous state change
```
export default ({ state, event }) => {
  event.preventDefault();

  return Object.assign({}, state, {
    [event.target.name]:event.target.value,
  });
}
```

> Action for every change in the target values.

Name: onSubmit
Type: Do Mutation
```
export default ({ state, event, eventComponentProps, history }) => {
  event.preventDefault();

  return async ({ getState, setState, mutate, getMutation }) => {
    setState(Object.assign({}, getState(), {
      loading: true,
    }));

    try {
      // set the date for the submitted message
      const addDateVariable = Object.assign({}, getState(), {
        date: new Date().toISOString(),
      });

      const response = await mutate({
        mutation: getMutation('addMessage'),
        variables: addDateVariable
      });

      setState(Object.assign({}, getState(), {
        title: "",
        description: "",
        error: null,
        loading: false,
      }));

      // change path to the newly created message
      history.push(`/message/${response.data.createMessage.id}`);
    } catch (e) {
      setState(Object.assign({}, getState(), {
        error: e,
        loading: false,
      }));
    }
  };
}

```

> Action for submitting the data gathered from the __Form__, setting the state back to it's default and send the user to the newly created
message. The __date__ property is added to the variables fetched from the inputs.

Now in the __Form__ component's configuration we add the event __onSubmit__ with the __onSubmit__ action created.

For the __title__ and __description__ inputs we go to each configuration and set the `Name` option as `title` and `description` respectively
and add the Event __onChange__ to the __changeField__ Action. For each of them in the PropsFlow tab add a Link for each property with the type __Value__.

For the button input we set the `Value` and `Type` as __Submit__.


### It still doesn't look pretty, but it works! Congratulations!
<br><br><br>
