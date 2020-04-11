# HTML + CSS Book
## Ch 6 Tables (126-145)
- \<table>
- \<tr> and \<td> table row and table data make up the table
- \<th> table heading 
- colspan attribute makes a row item spread across multiple columns
    - ex. \<td colspan = "3">Gym\</td>
- rowspan does the same thing except vertically, spanning multiple rows
- you can break long tables up w/ head, body, and foot 
    - ex. \<thead> \<tbody> \<tfoot>

# JS + JQuery Book
## Ch 3 Functions, Methods, and Objects (106-144)
- In addition to literal notation (pg 102) you can also use construction notation (pg 106)
    - ex. var hotel = new Object ();
    <br> hotel.name = 'Quay';
    <br> hotel.rooms = 40;
    <br> hotel.booked = 25;
    <br> hotel.checkAvailability = function() {
        <br> return this.rooms - this.booked;
        <br>
    };

- to update or add to an object, use dot or square brackets
    - ex. to chance hotel name
    - hotel.name = 'Park';
    - hotel['name'] = 'Park';
    - similarly you can delete w/ 
        - delete hotel.name;

- If you know you'll have to create multiple objects w/ the same format, use construction notation to make a templete:
    - function Hotel(name, rooms, booked) {
        <br> this.name = name;
        <br> this.rooms = rooms;
        <br> this.booked = booked;
        <br> this.checkAvailability = function(){
            <br> return this.rooms - this.booked;
            <br>
        }<br>
    };
    - and then to create a new object using that template you just created, use 
    <br> var quayHotel = new Hotel ('Quay', 40, 25);
    <br> var parkHotel = new Hotel ('Park', 120, 77);

- There are three groups of built in objects
    1. Browser Object Model - creates a model of the browser tab or window
    1. Document Object Model (DOM) - creates a model of the current web page
    1. Global Javascript Objects - group of individual objects that relate to different parts of the JS language