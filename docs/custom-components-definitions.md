---
id: custom-components-definitions
title: Custom Components API
sidebar_label: Custom Components API
---

## Default Component Code
Whether created with content in the tree, or as blank components, the outcome, from the components code perspective is the same.

The following is the code created by default for custom components:

```js
import React from 'react';
import PropTypes from 'prop-types';
import shiftComponent from '@shift-studio/shift-extension-react';

@shiftComponent
export default class ComponentDefinitionClass extends React.Component {
  static propTypes = {
    shiftProps: PropTypes.object.isRequired,
  };

  render() {
    const { shiftProps, ...ownProps } = this.props;

    return this.renderShiftChildren({
      props: ownProps,
    });
  }
}
```

Shift custom components work by decorating a component with a shift-extension and making calls to the methods that it provides as well as using data it may provided. This is why, whether created via the tree or as blank components, all components share the same default code. The content of each components tree is just a result of rendering its children, not a part of the definition itself.

# Shift Extension for React

## shiftProps
By decorating a component with the extension, the shiftProps object is passed into your component. This includes:

### selection
This object represents your current selection in the IDE.

```js
id: "169d68cca5ea68c17001a007"
rootInstances: Array[0]
keys: Array[0]
canvasId: "defaultCanvas"
```

### flowProps
This object contains the props passed through the Shift Component Tree.

### activeVariants
This object represents the active variant in the tree.

### editing
A boolean to indicate whether a use is in 'editing' mode or 'play' mode. This flag can be used to enable editing-experience only features in a component.
