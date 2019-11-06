---
id: component-tree
title: Component-Tree
sidebar_label: Component-Tree
---
The __Component Tree__ shows the hierarchical relationship between all the components in your app.

Each component in the three shows as an icon, component-type and text label for better identification.

Expand the components in the tree using the Arrow icon at its left in order to view and access its child components.

Icon decorators (see table below) are used to indicate whether a component is either stateful, triggers and event or even both.
((table with icons and meanings))

Right-click on an component in the tree to access the context menu for the selected component.

## Component Hierarchy
In the Shift's development environment it's important to have in mind that component hierarchy is what determines how data and access flows through the app. 

A parent Component will determine the scope available in its children components. Being it data binding, properties and content can be accessible by children and so visually it is a good way to understand how every components behave and share.

Always keep in mind that when deleting, copying or cloning a component you are deleting, copying and cloning not only its content but also its entire children structure, content, data and binding.

## Manage Components
To manage __Components__ a variety of manipulation options are available:

* __Drag'n'Drop__ - Every component in the Component-Tree can be dragged around to adjust the hierarchy Tree and for placement of the component in the __Canvas__ always with the help of highlight guidelines of the available droppable areas.
* __Creation Tool__ - A "Plus" button in the Component-Tree that will open the Creation Bar with all the available components ready to use in your project, to assign a component just click it or drag it and drop it in the desired place either on the __component-tree__ or __canvas__.
* __Context Menu__ - Right-click on a component for the context menu to show with a set of options for re-adjustment, cloning, copy, deletion, and others.

### Selected Component
To select a component just click it in the __Component-Tree__ or __Canvas__. It is important to know that when a component is selected all the panels (Settings, State, Props Flow) will update their information to this component.

You can only have a selected component at a time and this will be linked througout the __Component-Tree__, __Panels__ and __Canvas__


### Add Component
* Access the __Creation Tool__ by clicking the plus button in the __Sidebar__ or at the bottom left of the __Component-Tree__ panel
* Choose your component from the component list or search it in the search box.
* Select it or Drag in drop it to the desired location.

### Clone Component
* Right-click in the component to be cloned to get access to the context menu
* Select the __Clone Component__ option
### Delete Component

### Copy Component
* Right-click in the component to be copied to get access to the context menu
* Select the __Copy Component__ option
* A copy of the component is now available in your copy clipboard

### Import
To import a component as HTML just right-click the __Component-Tree__ and in the context menu select the __Import HTML__ option to procede with the component import via HTML.

## References

* [__Canvas__](canvas.md)
* [__Shortcuts__](shortcuts.md)
