# HTML & CSS 
## Ch 3 - Lists
- 3 kinds of lists:
    1. unordered list
    1. ordered list
    1. definition list (this one is a little different):
        - \<dl> \<dt> \<dd>
- Note - you can also nest lists within lists using proper indentation

## Ch 13 - Boxes
- CSS treats each HTML element as if it sits within it's own box
- With CSS, you can control the size of any box by assigning a height and width value - these values can be measured in pixels (px) percentages (%), or ems
    - pixels set a static size that holds across any size of browser
    - percentage sets size relative to the browser window or, if within another box, relative to the size of that larger box
    - ems sets size based on the size of the text within it
- But! What if someon has a HUGE or SUPER SMALL browser window? To ensure your text is still readable, you can set min or max width and height.
    - ex. min-width: 450px;

- But! What if the min-height or min-width is still too big for your browser? The text boxes will look like an overlapping mess UNLESS you use the **overflow property** (makes the content vertically scrollable, either hidden or with a visual scroll bar)

- Every box has 3 properties that can be controlled to adjust its appearance
    1. Border
    1. Margin
    1. Padding
- Borders
    - width can be thin, medium, or thick
    - style can be solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none
    - color can be any color
        - Instead of having to list out all three attributes each time, you can define them all at once as follows
            - border: thin solid blue;

- Padding (just set the size)
- Margin (same, just set size)
    - If you want to CENTER a box or content, use
        - left-margin: auto;
        - right-margin: auto;
        - and on older browsers, you might need to use
            - text-align: center;
            - * unless you give the box a width, these commands will simply stretch the box the width of the page

- The DISPLAY property
    - inline: moves onto one line; think nav bar
    - block: opposite of inline?
    - inline-block
    - none: hides the box entirely, you would have to view the source code to even know that it's there
    - Similar to 'none,' you can use the 'visibility' property and set it to 'hidden,' but this will leave an awkward white space over the hidden element

- ROUNDED CORNERS
    - Use border-radius: 10px;

# JS + JQuery 
## Ch 4 cont. Decisions and Loops
- Switch statements - honestly, not entirely sure why you would use a switch statement over an if...else statement

- Truthy Falsy values
    - as soon as code hits a truthy value, it executes that code block (short cirvuit values)
        - This is why it's best practice to put code most likely to return 'true' first in OR || operations, while it's best to put false answers first in AND && operations

- LOOPS
    - 3 kinds of loops:
        1. For loops: run a specific number of times
        1. While loops: run until they hit a false value
        1. Do...while loops: run until it hits a false value and runs that fals value once before it stops...?
