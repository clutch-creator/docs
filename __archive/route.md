---
id: route
title: Route
sidebar_label: Route
---

`"Its most basic responsibility is to render a specific component when a location matches the route’s path."`

## Component Settings
- [__Default Component settings__](components.md#default-component-settings)
- __Path__ - Specifies the pathname to be matched for the Route
- __Exact match__ - Specifies if the match for the __Path__ is to be exact
- __Default Path__ - Specifies the default path for the Route

<br>
### Path
`String`

If a __Route's__ path matches the current location, it's children Components will be rendered.

To determine if a Route component's path prop matches the current location, the [`path-to-regexp`](https://github.com/pillarjs/path-to-regexp) package is used. It compiles de path string into a regular expression which is matched against the current location pathname.

### Exact match
`boolean`

Presented by a checkbox, the option __Exact match__ assures that the match is equal to the __Path__ defined.

### Default path
`String`

Sets the default path for that __Route__. When using params such as `/user/:userid` if the userid in the current location is not matched, the default path will be returned.

## References

* __React Route__ -[reacttraining.com](https://reacttraining.com/react-router/web/api/Route)
* __path-to-regexp__ -[github.com/pillarjs/path-to-regexp](https://github.com/pillarjs/path-to-regexp)
