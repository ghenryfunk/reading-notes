## Ch 15 - Layout (pg 358-404)
### CSS LAYOUT!
- CSS has 3 positioning schemes:
    1. Normal flow (default)
        - ex. position: static;
    1. Relative Positioning (targets specific elements and leaves others in normal flow)
        - ex. position: relative;
    1. Absolute positioning (?)
        - ex. position: absolute;
- CSS has 2 box offset properties
    1. fixed positioning (position: fixed;)
    1. Floating elements (float: right;)
- Often, with fixed or absolute positioning you will have one element on top of another - to ensure they don't overlap, you can assign one to display over the other. This is done w/ the z-index
    - ex. z-index: 10;
- Floating elements (? see pg 370-376)
- Fixed width layout - design does NOT change as user changes the size of their browser window - measurements often in pixels
- Liquid layout - design does change as user changes size of browser - measurements often in percentages
- Grid layouts (? see pg 387-394)
    - good visual layout of most browsers, see these pages for reference
- You can use multiple style sheets to organize various parts of your website. You can reference multiple CSS files one of two ways:
    1. @import - using one link in your HTML, you cna then reference multiple CSS files from the main CSS file directly linked in your HTML
        - ex. (within the main CSS file) @import url("tables.css");
    1. You can also just have multiple links within your HTML file
        - ex. \<head> <br>
                     \<link rel="stylesheet" type="text/css" href="css/site.css"/> <br>
                     \<link rel="stylesheet" type="text/css" href="css/styles.css"/> etc. etc.