---
id: shift-component
title: Shift Components
sidebar_label: Shift Components
---

## Components

__Components__ are an application's building blocks. As so, the user should be able to build any application he wants with just components. There has been advances in the past few years on turning componentization a standard in web development. Web components have been evolving in that direction, and they are based on four main specifications:

- __Custom Elements__ - lays the foundation for designing and using new types of
DOM elements.
- __Shadow DOM__ - allows to use encapsulated style and markup in web
components.
- __HTML Imports__ - defines the inclusion and reuse of HTML documents in other
HTML documents.
- __HTML Template__ - enables the declaration of fragments of markup that go
unused at page load, but can be instantiated later on at runtime.

Although web components have been trying to keep up and provide a better experience for web developers, the difference to the end consumer is none. Another point is that there are other libraries that have been coming up such as `React`, Vue or Angular that provide a better development environment and already have a huge set of reusable components which gives them a major differentiation point.

Essentially a web component is composed of:

- Attributes
- Internal properties
- Logic
- Events
- HTML

This can be directly related to `React`, as in:

* Attributes -> Props
* Internal properties -> State
* Logic -> Logic
* Events -> Virtual Events
* HTML -> JSX


Reference: [React Components](https://facebook.github.io/react/docs/web-components.html)

>__Shift__ adopts a components convention that follows these exact base concepts, with the clear vision that it is a feature for developers and not for an user created application end users.

In theory you can create any type of component in `React` and have components with state, props and event render an entire application in a single component. Nothing stops developers from doing that, but there are a lot of benefits from splitting their application in multiple components:

- __Reusability__ - Small components are self contained and can be re used in
different parts of an application.
- __Performance__ - By dividing components you can prevent an application from
fully re rendering every time something in your state updates.
- __Readability__ - Faster to understand a small component that does only one
thing than a huge single component.
- __Maintainability__ - Changes or adding features get easier

Another concept used in React development is creating a distinction between Container and Presentational components. They are both normal React components but Containers are stateful and Presentational stateless. This separation is important as it promotes reusability and improves code readability and maintainability, reason being that it gets simple and intuitive to capture data flow as well as that presentational components are a result of consuming props only, meaning that given the same props they'll output the same thing every time.


## Shift Components

Components are a key part of __Shift__, they are used inside the [Builder](introduction.md). As so,  __Shift Components__ integrate __Shift's Builder__ and provide an interface that follows the best practices, not limiting the developer/user.

From our contex
Shift's Components are based in 5 main concepts:

- __Props__ - Defines which props the component can receive and what input option widget to use.
- __State__ - Defines how state is controlled, it can be done in the shift's builder interface. The component can deal with global state or even local state.
- __Logic__ - A component will most of the times have logic associated, examples are data fetching, conditional render, or any other logic for the component behaviour.
- __Events__ - Shift's Components are able to define custom events they might trigger, another aspect that scales options when building custom components.
- __Render (JSX)__ - This is our result, presentational or not, from all the logic, state, props and events bundled together.

__Shift components__ allow the developers to build custom components with a familiar interface and concepts (`React`) without limits and a clean toolset and flow.
