---
id: custom-component
title: Build a Custom Component
sidebar_label: Build a Custom Component
---
<br><br>



## Templates
### Component Template
All Shift Components are made of `React`, so if you are familiar with the paradigm you will have no trouble developing your own component.

```
import React, { Component } from 'react';
import PropTypes from 'prop-types';

export default class ShiftComponent extends Component {
  static propTypes = {
    renderChildren: PropTypes.func.isRequired,
    getAttributes: PropTypes.func.isRequired,
  };

  static defaultProps = {};

  render() {
    const { renderChildren, getAttributes } = this.props;

    return (
      <div {...getAttributes()}>
        {renderChildren()}
      </div>
    );
  }
}
```

* __propTypes__ -
    * __renderChildren__ -
    * __getAttributes__ -
* __defaultProps__ -

### Settings Template
Set your custom component place so it can be part of Shift.

```
export default {
  icon: '',
  type: types.PRESENTATIONAL,
  category: 'structure',
  childrenType: {
    default: {},
  },
  propsSchema: [],
};
```

* __icon__ -
* __type__ -
* __category__ -
* __childrenType__ -
* __propsSchema__ -
