---
id: qs-05-routes
title: Routes
sidebar_label: Routes
---

## Introducing Shifts Routing System
Shift's routing system is similiar to React-Router. Client-side routing allows you to harness all the benefits that the URL brings, from specific bookmarks to path parameters, while retaining all positives of having a Single Page Application.

## Routers
Continue where you left off or create a new project. With your component drawer open, add a Router to your App's tree.

A couple of things will happen besides a Router appearing in the tree; your canvases will receive a pathbar and by default two Routes with links to one another will be added as default children of the Router.

## Router-View
You'll also notice that next to the path bar is another new Button:  <img style="display: inline-block; height: 2rem" src="/docs/assets/routing-view-btn.png" />. Go ahead and click this.

<details open>
<summary>Fig 1</summary>
<img style='padding: 20px' src="/docs/assets/routing-view.png" />
</details>

You'll see the routing overview of your entire app this way. Every time you drop a router into your app, your routing tree will reflect all the branching and views you've created.

## The Component Set
By simply dragging out a router, you get exposed to the entire component set.

### Router
This component is required whenever using routes, and is the only component that routes will sit in.

### Route 
This component defines the routes themselves, the paths they match, and whether to only match when 'exact' rather than progressively.

### Link
This is similiar to the `<a>` tag in HTML. It differs in that the routing is internal to the routing engine but otherwise behaves similiarly.

All of these components are configured through their `props`.

## What are props?

So far, when accessing the component Editor, we've used the Styling tab. In addition to the Styling tab there is a 
settings tab. Here, is where you can modify properties on the component. Watch what happens if we're on the "/" route, and we uncheck exact from either route.

<details open>
<summary>Fig 2</summary>
<img style='padding: 20px' src="/docs/assets/exact-prop.gif" />
</details>

Notice it shows Route2, set to "/route2" even when at "/". That's because with 'exact' deselected, "/route2" matches "/", not exactly, but progressively, from left to right. Exact allows you to ONLY render an element when the path and the route are identical.

Most components have props and the props tab is where they can be accessed.
