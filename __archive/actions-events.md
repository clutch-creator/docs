---
id: actions-events
title: Actions/Events
sidebar_label: Actions/Events
---
## Events
`DOM Events are sent to notify code of interesting things that have taken place. Events can represent everything from basic user interactions to automated notifications of things happening in the rendering model.`<br> - MDN

With __Events__ it is possible to capture user interactions with the DOM. You can see it as a trigger to execute an __Action__.

Let's take the example of a user clicking a button to Hide or Show a Sidebar. Defining a `onClick` event enables the execution of an __Action__ when the button gets clicked. And in another case if a `onMouseOver` event was defined instead, the action would be executed everytime the button was being hovered by the mouse.


>There's a list of standard events defined in official specifications and you can investigate it in the [__References__](#references) section.


## Actions

Every event has its consequences, so do they in web development. We call __Actions__ to the code and/or functions that are executed and called by the __Events__.

So for our previous Hide/Show button example the __Action__ would be the code/function to execute for the Sidebar to Hide or Show accordingly, being it triggered by a mouse click or mouse or any other.

>There's a list of templates that are already implemented in __Shift__ that can be found in the [__Action Templates__](action-templates.md) page.

## References
* __Events__ - [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Events)
