---
id: styles
title: Styles
sidebar_label: Styles
---
`Styles sheets represent a major breakthrough for Web page designers, expanding their ability to improve the appearance of their pages.`<br> - W3.org

A __Style__ contains style information for a document, or part of a document. It enables you to convert text into images, control white spacing, tabling, colors, font size, alignment and many more.

By default, the style is expected to be written in [__CSS__](https://developer.mozilla.org/en-US/docs/Web/CSS).

<br><br>
_"The __CSS__ (__Cascading Style Sheets__) is a stylesheet language used to descrribe the presentation of a document written in HTML or XML (including XML dialects such as SVG or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media."_

There are two ways to style an element:
* Write CSS properties inline
* Create classes in CSS and add them to an element

__Shift__ also provides this two ways to style by either __writing CSS__ or __using a visual interface__ for selecting each CSS properties.

## StyleSheets
For better organisation the styles are organised in __StyleSheets__, normally separate files, for better reusing withing different pages. Not only that but on many use cases it is important to render a specific document in different ways (ex: different devices) and therefore have different styles organised in different ways.

__Shift__ has it's own way of handling this management.

With the help of a __Class Editor__ and __Style Editor__ it is possible to separate each component styling not only in classes for better reuse, but accessible in a way that makes the search for a specific Style much more easier. At each app development start everything is stored in a default __Stylesheet__ and can also be edited there. We made sure to connect all this tools so whenever you make a change in a place it will automatically be updated everywhere. If in need of separate files for style organising you can also create more __Stylesheets__ like in any web development environment. So you can see __StyleSheets__ like the librarys for style in your app, while with __Class Editor__ and __Style Editor__ is your library searcher and organiser.

### Access StyleSheets
* To access __StyleSheets__ open the __Code__ menu on the right sidebar
* Select __StyleSheets__

### Create new StyleSheet
* Access __StyleSheets__
* Click the __StyleSheets__ dropdown menu and select __Add StyleSheet__

### Remove StyleSheet
* Access __StyleSheets__
* Right click on the to be removed __StyleSheet__
* Select __Remove StyleSheet__

## Class Editor - Managing Classes
Classes are reusable styles that can be added to HTML elementsand they enable a single HTML element to have multiple different looks with CSS. __Shift__ applies this concept to __components__ rendering too.

The __Class Editor__ provides you a visual UI where you can create, delete and delete the classes in your project sepparated in two categories, __Applied__ and __All__.
Not only you can manage your classes but you can also have information on where each class is used and even apply __conditionals__.
### Access Class Editor
* To access the __Class Editor__ open Shift's __Builder__ and select a component.
* Open the __Class Editor__ tab in the __Sidebar__
### Applied Classes
In this category you can manage classes for a specific component. Remember that the first reason to have classes in the first place is to enable their re-use, so even if you are applying a class to a specific component, it will be available in the __All__ category for later re-use.
### - Create Class
* In the __Class Editor__ select the __Applied__ category
* Type the name of the class to be created
* Select __Add class only__ or if you want to create a class and style it, select __Add class and create style__
### - Rename Class
* In the __Class Editor__ select the __Applied__ category
* Select the three dots icon at the right of the to be renamed class
* Select __Rename Class__
### - Remove Class
* In the __Class Editor__ select the __Applied__ category
* Select the three dots icon at the right of the to be removed class
* Select __Remove Class__
### All Classes
In this category you have all the classes available to your project. You can search for any Class, edit or apply it to a selected component.
### - Search for a Class
* In the __Class Editor__ select the __All__ category
* Type the name of the class you wish to find


## Style Editor - Managing Styles
Styles are simply a group of CSS properties that are applied to dictate how an element is rendered. In this case how our components are rendered.


To easily style your components, __Style Editor__ offers a visual UI with a toolset of __CSS__ properties enabling you to style with just a few clicks and without writing any code.
From simple default __CSS__ properties to __Layout__, __Typography__, __Borders__ and __Effects__ to __CSS3__ __Shadows__, __Transforms__, __Flex__ __Box__ and __Media__ __Queries__.

### Access Style Editor
* To access the __Style Editor__ open Shift's __Builder__ and select a component.
* Open the __Style Editor__ tab in the __Sidebar__
### All Styles
In this category you have all the styles present in your project and you can search through them by typing a style name or create a new one by selecting the __Create style from search input__ option. It is possible also to edit a style by simply clicking it and also see its information and content preview.
### Applied Styles
In this category you have all the styles that are applied to the selected component. You can edit a style by simply clicking it and also see its information and content preview.
### Preview
The changes in style will automatically be applied and thanks to the __live preview__ of __Shift__ you can see its changes directly on the __Canvas__.

### Import
It is also possible to import raw CSS in the __Style Editor__ by simply copying it to the __Raw CSS__ section at the bottom.



## Media Queries
_"Media queries are useful when you want to apply CSS styles depending on a device's general type (such as print vs. screen), specific characteristics (such as the width of the browser viewport, or environment (such as ambient light conditions). With the huge variety of internet-connected devices available today, media queries are a vital tool for building websites and apps that are robust enough to work on whatever hardware your users have."_ - MDN
__Shift__ provides its own manager to help forging your own media queries with a simple interface.

It is possible to __name__ a media query, select its __type__, add __values__ and still use the __AND__ and __OR__ conditions.
The media Query will stay stored in the previously chosen __Class__ selector and will have its own style properties.


### Media Query Manager
__Shift__ provides its own manager to help forging your own media queries with a simple interface.

It is possible to __name__ a media query, select its __type__, add __values__ and still use the __AND__ and __OR__ conditions.
The media Query will stay stored in the previously chosen __Class__ selector and will have its own style properties.

### Access Media Query Manager
* Create a new class or edit an already created class in the __Class Editor__ 
* It will open the __Style Editor__ in the chosen class selector
* Select Add Media Query
### Create a media query
* Access the __Media Query Manager__
* Select __Add Media Query__
* Select __Create Media Query__
* Type a name for the new media query as __Media Query Label__
* Select the a specific type of query or the All option
* Add Features to the type with the chosen Value and Amount
* Optionaly you can __Add OR condition__ to apply a __OR__ condition
* When finished select the __Create__ Button at the bottom right
### Edit or Delete media query
* In the __Class Editor__ access the class in which you want to edit or delete a media query 
* It will open the __Style Editor__ in the chosen class selector
* Select __Add Media Query__
* Click the "gear" icon at the right of the media query to be edited or deleted
* It will open the __Media Query Manager__ with the selected media query
* Edit or Delete the media query and click __Save Changes__ or __Delete Media Query__ when finished


## References
* __Media Queries__ - [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries)
* __StyleSheets__ - [w3.org](https://www.w3.org/TR/html401/present/styles.html)
<br><br><br>
