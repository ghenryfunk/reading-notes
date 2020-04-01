# HTML & CSS 
## Ch 4 Links (pg. 74-93)
- Links use the anchor element
    - \<a href="http://www.imdb.com">IMDB\</a>
- Links can be nested within other elements
- To link to other pages within the same website, use a *relative url* 
    - ex. \<a href="about-us.html">About\</a>
    - \*If you want to navigate through multiple folders (depends on how you've structured your site) simply use / to create a map for the relative link
- To create an e-mail link
    - \<a href="mailto:jon@gmail.com">Email Jon\</a>
- If you want to ensure your user opens links in a *new window* use the 'target' attribute
    - ex. \<a href="http://www.imdb.com" target="_blank">IMDB\</a>
- You can link to a specific part of the same page with two steps
    1. assign an id attribute to the HTML element you want to link to 
        - ex. \<h2 id="bio">Bio\</h2>
    1. then use the anchor tag with the id attribute
        - ex. \<a href="#bio">Bio\</a>
- If you want to link to specific parts of OTHER pages, use the regular link or relative link, and add /#id to the end
    - ex. \<a href="http://www.imdb.com/#bottom">Click Here to go to the bottom of the IMDB website\</a>

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

# JS & JQuery
## Ch 3 - Functions
- Functions perform a specific task
    - Two steps are needed (not necessarily in order)
        1. Declare a function
            - ex. function sayHello(){
                document.write('Hello!'); <br>
            }
            - ex. sometimes functions require parameters: <br> ex. function getArea(width, height){<br>
                return width*height;<br>
            }
        1. Call a function
            - ex. sayHello();
            - when the function requires parameters, you have to add values (known as arguments) when calling the function <br> ex. getArea(3,5); <br> or <br> wallWidth=3;<br>
            wallHeight=5;<br>
            getArea(wallWidth, wallHeight);
    - If you want a function to RETURN a single value, then use the 'return' keyword
        - ex. function calculateArea(width,height){<br> var area=width*height;<br>return area;<br>
        }<br>var wallOne=calculateArea(3,5);<br>var wallTwo=calculateArea(8,5);
    - If you want a function to *return multiple* values, use an array
        - ex. function getSize(width, height, depth){<br>var area=width*height;<br>var volume=width*height*depth;<br>var sizes =[area, volume];<br>return sizes;<br>}<br>var areaOne = getSize(3,2,3)[0];<br>var volumeOne = getSize(3,2,3)[1];
    - Variable Scope
        - Variables can either be
            1. local - declared within a function
            1. global - declared outside a function
        - \*use local variables when able as they require less memory/load time than global variables

# 6 Reasons for Pair Programming by Allie Grampa (on codefellows.com)
1. greater efficiency
1. engaged collaboration
1. learning from fellow students/coders
1. social skills
1. job interview readiness
1. work environment readiness
    - \*I'm sold!