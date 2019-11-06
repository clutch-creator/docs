---
id: qs-04-symbols
title: Symbols
sidebar_label: Symbols
---

## Where we're at

So you've used and nested a couple of components. You've modified the content of text and styled the block.

### Whats next?

Shift is an incredibly powerful platform in that it not only lets you create your UI, but allows you to build an entire sophisticated design system. Lets go back to the components tree view by clicking on  <img style="display: inline-block; height: 2rem" src="/docs/assets/components-tree-icon.png" /> . Then right-click on your Block component in the tree and select 'Create Component' and name it.

<details open>
<summary>Fig 3</summary>
<img style='padding: 20px' src="/docs/assets/create-symbol.gif" />
</details>

Notice, in the Symbols pane, we now have your newly created Symbol in addition to App. In the App canvas, the tree of components has been replaced with the symbol as well. Visually nothing has changed however.

## What is a Symbol?

Your component is now a symbol. If you look in your components tray you will see it in there. Symbols allow designers to create new reusable parts and make them available for use throughout your app. All changes you make to your Symbol will be reflected across all instances of that Symbol in your project. 

Your canvas is now showing the canvas for that symbol. Symbol trees and Symbol canvases are unique in certain ways. You are allowed to bring multiple instances of the symbols into these trees and their respective canvases. This allows you to view your component in multiple states, add documentation, provided visual context (what good is designing a full width button thats expected to go in 240px container, when it's streching across the whole page). At the end of the day, only the contents inside the symbol are 'exported' out (as seen in App, where our new component is beings used.)

Go ahead and change some styling on the Block and Text elements in the Symbol and head back over to the App to see that Button reflect those changes.

## Variants

Select the top block in your Symbol. (It will be purple). Head over to the component editing tab and click 'Add Variant'. Let's name this Variant 'warning'.

With the 'warning' variant selected, go ahead and change your styling.

Switching back to the App symbol, note that the Symbol you made, doesn't reflect the changes you just made. However, if you pick the symbol in the tree and head to the Component Editor view, notice you are able to select a variant now.

In this way, like-components can be sensibly grouped.

In a way it's like CSS classes, where `.btn`,`.btn .active`, and `.btn .disabled` might be used to modify a set of elements into fulfilling multiple purposes. The main benefits being the encapsulation of the styling to the component (this inadvertly gets rid of the 'naming' issues that CSS is known for) as well as the extended functionality that variants bring: events and props by variant. 

## Conditionally Applying Variants
As you've seen, variants can drastically alter the appearance of a component. Like classes, they can be combined and rearranged for even more flexbility and contol.

However, its not uncommmon to need a component to change variants. For example, a submit button may be 'disabled' until a form is completed and then 'default' when ready. 

It is for this reason that variants can be applied conditionally.

On an instance of a Symbol go ahead and pick the Components editor. Click on the the expansion for the Variant you'd like. There you will find a series of Props you can directly bind to as well as an option to use a "module", a context-aware bit of code, to create the condition logic if something more complex is needed. 
