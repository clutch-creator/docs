---
id: state
title: State
sidebar_label: State
---
`State is best described as how a component's data looks at a given point in time`

As a concept from __React__ that is part of __Shift__, State is used so that a component can keep track of information within its own environment or the wider app environment.

__What happens when a component receives data from other components than the parent?__

__What if the user changes and/or inputs data directly to the component?__

To answer this, we have __State__.

So state is used so that a component can keep track of information in between its renders. When you apply changes to __State__ it updates and re-renders the component. 

Imagine a search bar component for example. It will have changes according to user input. Everytime we set a new input in a search bar we want to provide and show the results that match the search to the user. This can be done with __State__ making the component update every time it gets a change in the search bar or just when a button is pressed or trigger it by another input, complete control over the component rendering.

__State__ is not mandatory in every component, just if the component implys changes.

So normally a distinction is made for components that don't have __State__ and therefore are referred as __stateless__ and components that do have it and are known as __stateful__.


>For more on __stateless vs stateful__ or __presentational vs container__ components refer to the [__Everything as Components__](everything-components.md) section.

In __Shift__ we have a way of expressing state in two different types, __Local__ and __Global__ state.

When we want a component to just deal with state for internal cases like a button change, a toggle, a different filter or a form submission we use __Local State__, and for when we need different components to communicate each state changes to one another we use __Global State__.

## Local  State
When a component handles just the changes which he is responsible for, we are dealing with __Local State__.

In a button, checkbox or toggle example, the state only needs to be managed inside the component in order to handle user input, change its data and handle rendering. And in this case we will be looking at two useful __Local State__ states. ((couldn't help it))

### Default State
The state default values. Once a component is mounted the state is initialised with this values.
### Current State
Every update and change will be represented by the __Current State__, it is also what information which the component will render.

## Global State
In order to communicate and maintain __State__ throughout different components __Global State__ joins the fight. 

In a example where we want to share data between components that work together but are not parent or child of one another we need to connect this two using __Global State__.

For better reuse of __Global State__ this is presented with __Scopes__ which are determine which state properties are shared across components.

### Scope

### Select Type
### Map Type
### Advanced Map Type

## References
* __State FAQ__ - [reactjs.org](https://reactjs.org/docs/faq-state.html)
<br><br><br>
