---
id: link
title: Link
sidebar_label: Link
---
The primary way to allow users to navigate around your application. 


## Component Settings
- [__Default Component settings__](components.md#default-component-settings)
- __Link__ - link's destination URL. Can be absolute or relative.
- __Target__
    * __Self__ - Opens the linked document in the same frame as it was clicked (this is default)
    * __Blank__ - Opens the linked document in a new window or tab
    * __Parent__ - Opens the linked document in the parent frame
    * __Top__ - Opens the linked document in the full body of the window




## Default children
* Text - [__Text__](text.md)(`Component`)

## Notes
- A __Link__ can know when the route it links to is active and automatically apply an `activeClassName` and/or activeStyle when given either prop. The __Link__ will be active if the current route is either the linked route or any descendant of the linked route.

- A string literal can be used as the `Link` option.

## References
 * __Link__ -[developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link) - MDN
