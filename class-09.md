# HTML + CSS 
## CH 7 Forms (pg 144-175)
- several types of form controls:
    - adding text (text input, pw input, text area)
    - making choices (radion buttons, checkboxes, dropdowns)
    - submitting forms
    - uploading forms

## CH 14 Lists, Tables, and Forms
- If you want to use bullets outside the text box w/ CSS
ul {
  list-style: outside disc; }
- Table styling see pg 338


# JS + JQuery book
## Ch 6 Events (pg 243-292)
- Events are "fired" or "raised" by user interface with the web browser
    - UI, keyboard, mouse, focus, form, or mutation events

- Events trigger JS code w/ 3 steps (known as Event Handling)
    1. select element
    1. specify event (called 'binding')
    1. call code

- The recommended way to bind an event to an element is using Event Listeners (pg 254)

- Event flow matters when your code has event handlers on an element AND one of its ancestors or descendent elements

- When an event occurs, the event object tells you information about the event and the element it happened on
- Creating event listeners for binding an event to MANY elements can slow down a web page, but you can use event Flow to listen for an event on a parent element...?
- The event object has methods that change - so you can manipulate the default behavior of an element
- When calling a function, the event objects target properly is the best way to determine which element the event occured on. But you may see the 'this.' keyword used
