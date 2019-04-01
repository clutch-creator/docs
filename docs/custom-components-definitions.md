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

Shift custom components work by decorating a component with a shift-extension and making calls to the methods that it provides as well as using data it may provide. This is why, whether created via the tree or as blank components, all components share the same default code. The content of each components tree is just a result of rendering its children, not a part of the definition itself.

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
This object contains the props passed through the Shift Component Trees prop flow.

### activeVariants
This object represents the active variant in the tree.

### editing
A boolean to indicate whether a user is in 'editing' mode or 'play' mode. This flag can be used to enable editing-experience only features in a component.

## Methods
The shift extension also attaches several methods to your component instances.

<AUTOGENERATED_TABLE_OF_CONTENTS>

### `renderShiftChildren({props: Object, area: String})`
This renders your components hierarchy (it's tree). It takes two properties:

#### props: Object
This is the object you want to pass into the application Props Flow, this will be available to all of the children of this component to bind to.

#### area: String (optional)
Use this property to render into a specific renderArea, 'default' is used by default or if one is not provided. Remember to configure any render areas used (besides 'default') in the components settings. Each area added will create an additional place to drop children in the app's tree.

### `getShiftAttributes(passThroughAttributes: Object)`
This is designed to be used for presentational components. It links the Shift styling interface to the component, passing along the attributes created or bound in the IDE to the rendered component. It takes one optional parameter, `passThroughAttributes`, which should include any passed properties that you want passed to the underlying component. This allows you to blend Shift attributes with external attributes.

```jsx
...
render {
  return (
    <div {...this.getShiftAttributes()}>
      {this.renderShiftChildren()}
    </div>
   )      
}
```

### `bindShiftModule(moduleID: string)`
If you selected 'module' as a PropType for your component you will have to take the ID passed as a String and pass it to this method. Afterwards, you can make a call to that bound module.

```jsx
...
render {
  const { logicModule } = this.props;
  
  const logic = this.bindShiftModule(logicModule);
  
  return (
    <MyComponent logic={logic} {...this.getShiftAttributes()}>
      {this.renderShiftChildren()}
    </MyComponent>
   )      
}
```