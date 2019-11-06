---
id: action-templates
title: Actions Templates
sidebar_label: Actions Templates
---



## Templates
### Synchronous state change
```
export default ({ state, event, eventComponentProps, history }) => {
  event.preventDefault();

  return Object.assign({}, state, {
    // changes
  });
}
```


### Synchonous state change from input
```
export default ({ state, event }) => {
  event.preventDefault();

  return Object.assign({}, state, {
    [event.target.name]: event.target.value,
  });
}
```

### Asynchronous state change
```
export default ({ state, event, eventComponentProps, history }) => {
  event.preventDefault();

  return async ({ getState, setState, mutate, query, getQuery, getMutation, client }) => {
    setState(Object.assign({}, getState(), {
      loading: true,
    }));

    // do async operations

    setState(Object.assign({}, getState(), {
      loading: false,
    }));
  };
}
```

### Do Mutation
```
export default ({ state, event, eventComponentProps, history }) => {
  event.preventDefault();

  return async ({ getState, setState, mutate, getMutation }) => {
    setState(Object.assign({}, getState(), {
      loading: true,
    }));

    try {
      const response = await mutate({
        mutation: getMutation('YOUR_MUTATION_NAME'),
        variables: {
          // mutation variables
        }
      });

      setState(Object.assign({}, getState(), {
        error: null,
        loading: false,
      }));
    } catch (e) {
      setState(Object.assign({}, getState(), {
        error: e,
        loading: false,
      }));
    }
  };
}
```


### Update query from subscription
```
export default ({ state, event }) => {
  return async ({ client, getQuery }) => {
    const query = getQuery('YOUR_QUERY_NAME');
    const data = client.readQuery({
      query,
    });

    client.writeQuery({
      query,
      data: {
        // new data to update query apollo cache
      },
    });
  };
}
```
<br><br><br>
