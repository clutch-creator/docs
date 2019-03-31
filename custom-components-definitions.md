---
id: custom-components-definition
title: Custom Components Definition
sidebar_label: Custom Components Definition
---

# Default Entry Definition
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
