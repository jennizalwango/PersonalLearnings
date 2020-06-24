The Document Object Modal

The Dom helps  to connects  web pages to scripting languages by represnting the structure of the document. Its bascially helps you access, update the content , stucture and the styles of Document. 

The DOM is represented into 3 parts

    

- Core DOM -  for all document types
- XML DOM -  for XML documents
- HTML DOM -   for HTML documents.

HTML DOM

the HTML  dom is a standard object model and programming interface for HTML . The dom defines , the following;

Properites of html elements.

Methods to help access HTML elements, 

Events for all HTMl elements  and Objects.

HTML methods are actions you can prefom on the html elements eg adding or deleting an element. example `geElementById()`

HTML properites are the values of Html that you can set or change. like changing, updating content on the document. ``innerHTML`

`innerHTML` -- is used to rplace or get content of an HTML element.

Note: if you want to access any element in the web page you have to start with the `document `keyword eg document.getelement by id.. This is represnts your page.

**Events**

In javacsript the interaction with HTML is handled through  ****events** that occur when the user or the browser manipulates a page. When the page loads, it is called an **event**. When the user clicks a button, that click too is an **event**. Other examples include **events** like pressing any key, closing a window, resizing a window

Through the DOM javascript is able to react to events. Javascript can be executed when an event occurs, eg

`onload`,  `onClick`,  

`onload` and `onunload` events are triggered when the user enters or leaves the page.

Some HTML events are ;

- When a user clicks the mouse
- When a web page has loaded
- When an input field is changed

**EventListeners**

`addEventListner()`  is a method triggered when an event occurs, it attaches an event handler to the specificed elemnet(explain the process of events and how they happen)

The `addEventListener()` method makes it easier to control how the event reacts to bubbling(This relates to the order in which event handlers are called when one element is nested inside a second element. So here the event is first captured and handled by the most innermost element ). And  with capturing is (the event is first captured by the outermost element and propagated to the inner elements)

The `addEventListener()` method allows you to add many events to the same element, without overwriting existing events.
