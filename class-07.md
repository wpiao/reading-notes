# Read: 07 - HTML Tables, JS Constructor Functions - 1/30/2021

## HTML Tables  

- Example:
  ```HTML
  <table>
    <tr> <!-- table row -->
      <th></th> <!-- table heading -->
      <td></td> <!-- table data -->
      <td></td> <!-- table data -->
    </tr>
  </table>
  ```
- Spanning rows - `rowspan="2"`
- Spanning columns - `colspan="2"`
- `<thead>` - heading of the long table
- `<tbody>` - body of the long table
- `<tfoot>` - footer of the long table  

## JS Constructor Functions
- Create an object, then add properties & methods
  1. Literal notation 
    ```JavaScript
    const hotel = {};
    hotel.name = 'Quay';
    hotel.rooms = 40;
    hotel.booked = 25;
    hotel.checkAvailability = function() {
      return this.rooms - this.booked;
    };
    ```
  2. Object constructor notation  
    ```JavaScript 
    const hotel = new Object();
    hotel.name = 'Quay';
    hotel.rooms = 40;
    hotel.booked = 25;
    hotel.checkAvailability = function() {
      return this.rooms - this.booked;
    };
    ```
- Create an object with properties & methods  
