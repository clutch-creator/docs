---
id: qs-02-intro-to-components
title: Introduction to Components
sidebar_label: Introduction to Components
---

## What is a component?

Components are the building blocks that make up your webapp. Everything represented visually in your app will be a component. Let's start by adding a 'Block' component, you can think of these as `divs` from HTML.

## Adding a component

Open the Components Drawer by clicking on the <img style="display: inline-block; height: 1rem" src="/docs/assets/add-component-btn.png" /> button along the toolbar. This will slide open the Components Drawer. 
<details open>
  <summary>Fig 1</summary>
  <img style='padding: 20px' src="/docs/assets/open-component-drawer.gif" />
</details>

Simply click a `Block` component to add it to your app, or drag it into your Canvas or Components Tree.
<details open>
  <summary>Fig 2</summary>
  <img style='padding: 20px' src="/docs/assets/add-block.gif" />
</details>

As you can see, your Components Tree now has one item: `Block`. Blocks, like divs, don't really do much on their own, so lets add some more Components.

## Nesting Components
With your block selected in the tree, open your Components Drawer again (feel free to hit <kbd>a</kbd> on your keyboard to quickly toggle the Components Drawer) and click on Text. Alternatively, you can drag the `Text` component from the Drawer into the `Block` in the tree or canvas.
<details open>
  <summary>Fig 3</summary>
  <img style='padding: 20px' src="/docs/assets/add-text-component.gif" />
</details>

This is similiar to the following html:

```html
<div>
  <p>Click to edit text.</p>
</div>
```

Except of course, expressed visually.

## Editing Text Components

Next, we'll want to edit the content of the text component itself. Simply double clicking the existing text will enable text editing.

<details open>
  <summary>Fig 4</summary>
  <img style='padding: 20px' src="/docs/assets/editing-text.gif" />
</details>
