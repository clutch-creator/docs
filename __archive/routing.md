---
id: routing
title: Routing
sidebar_label: Routing
custom_edit_url: test
---
`Routing is the set of rules that match the URL where the user is with what you want to show in your Application`
<br><br><br>

## Static Routing
In a static page environment every link and location changes would be relative to a file and filename. A page for each location (ex: About, Contacts, Home, etc.) and in each page different elements are to be shown or even in some cases the same element to be shown across different pages.

For that purpose static pages navigation has some disadvantages, you can't easily reuse code and functionality because you need to define each element in every page. Another issue would be for the navigation handling control, since any page url would be accessible without easy filtering and in case the user steps in a malformed url, the good old 404 page would take place, aswell as many other issues.

Imagine for example a Header from a page, a "fixed navigation menu" let's say, you would have to replicate the code to any page using this fixed menu (usually every page), re-configure every link in each header and if for some reason any of this went wrong, you wouldn't have a fallback system, a default path or filter to handle any of it.

## Dynamic Routing

Every web application is composed by multiple locations too, but with the concept of __Dynamic Routing__ it gets easier, quicker and safer to navigate. 

In __Shift__ you have __dynamic routing__ where there are no pages, but instead you have [__Components__](compoments.md) being rendered conditionally to whether a specified path matches the current browser URL. 

If looking at the same Header example using __Shift's__ dynamic routing, to have a component that we want rendered in every location, we set it once to match a set of url paths and in those paths and locations the component will be rendered. That way the Header will be rendered no matter the additional content of each location. We can also set a default path in case the url is malformed, and many other features, quicker, simpler and re-using.

To change what your app shows according to the current URL you have routing components. These components allow you to conditionally render a set of components based on the current URL. What this means is that they will only render the components inside them if a given `path` property matches the current URL. This allows you to have components that are visible in any URL path, and parts that only render for certain URLs
<br><br>
__Routing components__:
* [__Router__](router.md)
* [__Route__](route.md)

Let's learn from an example:

| Label  | Path    | Component | Exact match |
|--------|---------|-----------|-------------|
| HomeRoute | /       | Home      |     <center> x  </center>    |
| UserListRoute | /users  | UsersList     |             |
| LogoutRoute | /logout | Logout    |             |

If the location for the application was:

| Path                         | Match                                                           |
|------------------------------|-----------------------------------------------------------------|
| https://www.myapp.com/       | It would match the HomeRoute and render Home component          |
| https://www.myapp.com/users  | It would match the UserListRoute and render UsersList component |
| https://www.myapp.com/logout | It would match the LogoutRoute and render Logout component      |

>HomeRoute is configured with __Exact match__ otherwise it would match the other Routes and only render Home component no matter the path, since all the paths start with '/'

In case the path gets specific, and a path to a specific user is needed like  `/users/:userid`  __Nested Routes__ should be used.

## Nested Routes

The path `/users/:userid` should not be included in the __Router__ list because it would match the UserListRoute, and that's not its purpose.

In this case we use __Route__ components as children of the __UserListRoute__ to better specify the matching.

| Label    | Path           | Component  | Exact match |
|----------|----------------|------------|-------------|
| Userlist | /users         | UserList   |      <center> x  </center>      |
| UserRoute     | /users/:userId | SingleUser |             |

If the location for the application was:

| Path                                | Match                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| https://www.myapp.com/users         | It would match the UserListRoute and render UsersList component                               |
| https://www.myapp.com/users/:userId | It would match the UserRoute and render SingleUser component with the `userId` as a parameter |

This way when rendering the UserListRoute it will render the UserList component if the match is __Exactly__ `/users` and the UserRoute uses a
__path param__ to capture the pathname part after.

>Routes that share a common prefix should be grouped in the same component. Not only for better structure, since it makes parent Routes simple, but to render content that is common across every route with the same preffix

## Path Params
For situations where it is important to capture variables in a pathname we use Path params.

In the `/users/:userId` case, the `:userId` means that the part of the pathname that comes after `/users/` will be captured.

All the variables captured in a __Route__ will be stored in its `match.params`object and in this case `match.params.userId`.

In __Shift__ this `match` object will be part of the [__PropsFlow__](propsflow.md) in the __children__ components of the matched __Route__. It means you can access this captured parameter with:
```
props.match.params.userId
```


## Links

Normal HTML Links would enforce a page reload, since we are building an application and we can do this without reloading the entire page, we use the __Link__ component instead.

__Shift__ provides a [__Link__](link.md) component which is an extended version of the standard <Link> component from __React Router__.

For more on __Link__ usage check the [__Link__](link.md) component page.

## References


* [__Router__](router.md)
* [__Route__](route.md)
* [__Link__](link.md)
* __React Router__ - [reacttraining.com](https://reacttraining.com/react-router/)
* __Dynamic Routing__ - [reacttraining.com](https://reacttraining.com/core/guides/philosophy/dynamic-routing)

<br><br><br>
