# JS & JQuery Book
## Ch 3 Objects (100-105)
- Objects group together a set of variables and functions
    - variables become known as properties
    - functions become known as methods
    - ex. of object (object is hotel)
\ var hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25,
    gym: true,
    roomTypes: ['twin', 'double', 'suite'],
    checkAvailability: function(){
        return this.rooms - this.booked;
    }
};

- You can access the properties or methods of an object one of two ways
    1. Dot notation
    1. Square brackets

## Ch 5 Document Object Model (183-242)
- Instead of reading our HTML, CSS, and JS files, browsers create a DOM that models our code in a DOM tree
    - This allows the programs and scripts to talk to one another
    - * DOM is known as an API (application programming interface)
- The DOM tree consists of 4 types of nodes
    1. The document node (ex. \<!DOCTYPE>)
    1. Element nodes (ex. \<html>, \<body>, \<div>, \<h1> thru \<h6>, \<li> etc.)
    1. Attribute nodes (ex. id="___", script="____")
    1. Text nodes (ex. what you actually write between p tags)
- pg 186-7 GREAT VISUAL
- Accessing and updating the DOM has 2 steps
    1. Access the elements
    1. Work w/ those elements
- When you access an Element, it can return a **single** element node, or a **nodelist**
    - Methods that return a single element node: ex. getElementById('id') or querySelector('css selector')
    -Methods that return a nodelist: ex. getElementsByClassName('class') or getElementsByTagName('tagName') or querySelectorAll('css selector')
- There are two ways to select an element from a Nodelist
    1. The item() method
    1. using array syntax (preferred) pg 199
        - ex. var elements = document.getElementsByClassName('hot');
        if (elements.length >= 1) {
            var firstItem = elements [0];
        }
-If you want to run through all nodes in a nodelist, just add a 'for' loop 
    - ex. var hotItems = document.querySelectorAll('li.hot');
    for (var i = 0; i < hotItems.length; i++){
        hotItems[i].className = 'cool';
    }
- When you have an element node, you can select another element in relation to it using:
    1. para+Node
    1. previousSibling
    1. nextSibling
    1. firstChild
    1. lastChild
- Many browsers add a text node when they come across whitespace
- elements can have many nodes.
    - *If you want to just access tet nodes ex. nodeValue pg 212 & 214
    - *If you want to access the containing element ex. innerHTML (pg 220) or textContent (pg 216) or innerText (pg. 216)
- Two very different approaches to adding and removing content from a DOM tree
    1. The innerHTML property - best suited for updating entire fragements
    1. DOM manipulation - easily targets individual nodes in the DOM tree
- If you add HTML to a page using innerHTML, be aware of cross-site scripting attacks or XSS
- You can access and change an element's attributes w/
    - getAttribute()
    - hasAttribute()
    - setAttribute()
    - removeAttribute()
    