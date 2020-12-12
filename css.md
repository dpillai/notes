
1. https://www.freecodecamp.org/news/an-animated-guide-to-flexbox-d280cf6afc35/

2. Properties for the flex containers:

    1. There are several options for how to space the flex items along the line that is the main axis. One of the most commonly used is ```justify-content```. options include:

        - ```flex-start```  : aligns items to the start of the flex container. For a row, this pushes the items to the left of the container. For a column, this pushes the items to the top of the container. This is the default alignment if no justify-content is specified.
        
        - ```flex-end```    : aligns items to the end of the flex container. For a row, this pushes the items to the right of the container. For a column, this pushes the items to the bottom of the container.
        - ```space-between```   : aligns items to the center of the main axis, with extra space placed between the items. The first and last items are pushed to the very edge of the flex container. For example, in a row the first item is against the left side of the container, the last item is against the right side of the container, then the remaining space is distributed evenly among the other items.
        - ```space-around```    : similar to space-between but the first and last items are not locked to the edges of the container, the space is distributed around all the items with a half space on either end of the flex container.
        - ```space-evenly```    : Distributes space evenly between the flex items with a full space at either end of the flex container


    2. CSS offers the ```align-items``` property to align flex items along the cross axis. For a row, it tells CSS how to push the items in the entire row up or down within the container. And for a column, how to push all the items left or right within the container. The different values available for align-items include:
        - ```flex-start```: aligns items to the start of the flex container. For rows, this aligns items to the top of the container. For columns, this aligns items to the left of the container.
        - ```flex-end```: aligns items to the end of the flex container. For rows, this aligns items to the bottom of the container. For columns, this aligns items to the right of the container.
        - ```center```: align items to the center. For rows, this vertically aligns items (equal space above and below the items). For columns, this horizontally aligns them (equal space to the left and right of the items).
        - ```stretch```: stretch the items to fill the flex container. For example, rows items are stretched to fill the flex container top-to-bottom. This is the default value if no align-items value is specified.
        - ```baseline```: align items to their baselines. Baseline is a text concept, think of it as the line that the letters sit on.

    3. CSS flexbox has a feature to split a flex item into multiple rows (or columns). By default, a flex container will fit all flex items together. For example, a row will all be on one line. However, using the flex-wrap property tells CSS to wrap items. This means extra items move into a new row or column. The break point of where the wrapping happens depends on the size of the items and the size of the container. CSS also has options for the direction of the wrap:


        - ```nowrap```: this is the default setting, and does not wrap items.
        - ```wrap```: wraps items from left-to-right if they are in a row, or top-to-bottom if they are in a column.
        - ```wrap-reverse```: wraps items from right-to-left if they are in a row, or bottom-to-top if they are in a column.
    4. The ```order``` property is used to tell CSS the order of how flex items appear in the flex container. By default, items will appear in the same order they come in the source HTML. The property takes numbers as values, and negative numbers can be used.
    5. The ```align-self```property allows you to adjust each item's alignment individually, instead of setting them all at once. This is useful since other common adjustment techniques using the CSS properties float, clear, and vertical-align do not work on flex items. ```align-self``` accepts the same values as ```align-items``` and will override any value set by the align-items property.
3. Properties for flex items:
    1. The first is the ```flex-shrink``` property. When it's used, it allows an item to shrink if the flex container is too small. Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it. 
        - The ```flex-shrink``` property takes numbers as values. The higher the number, the more it will shrink compared to the other items in the container. For example, if one item has a flex-shrink value of 1 and the other has a flex-shrink value of 3, the one with the value of 3 will shrink three times as much as the other.
    2. The opposite of ```flex-shrink``` is the ```flex-grow``` property. Recall that flex-shrink controls the size of the items when the container shrinks. The flex-grow property controls the size of items when the parent container expands.
    3. The ```flex-basis``` property specifies the initial size of the item before CSS makes adjustments with ```flex-shrink``` or ```flex-grow```. 
        - The units used by the ```flex-basis``` property are the same as other size properties (px, em, %, etc.). The value auto sizes items based on the content.
    4. There is a shortcut available to set several flex properties at once. The flex-grow, flex-shrink, and flex-basis properties can all be set together by using the flex property. For example, ```flex: 1 0 10px;``` will set the item to flex-grow: 1;, flex-shrink: 0;, and flex-basis: 10px;
        - The default property settings are ```flex: 0 1 auto;```.

CSS GRID
1. Apply ```display: grid;``` to element to apply css grid.
2. Parent element is called contrainer.
3. Apply ```grid-template-columns: 100px 100px 100px;``` to define the number and size of columns. Same for ```grid-template-rows: 50px 50px;```.
    - ```grid-template-columns: auto 50px 10% 2fr 1fr;```
4. To have spacing betweens columns ```grid-column-gap: 10px;``` Same for rows.
    - You can use ```repeat``` function like
    ``` grid-template-columns: repeat(x times, 50px);``` or ```    grid-template-columns: repeat(2, 1 fr 50px) 20px;```
        - ```auto-fill``` to create as many columns/rows within the container instead ofspecifying the number. For e.g. ```repeat(auto-fill, minmax(60px, 1fr));```. Note: Repeat does not repeat the items of the container. So remaining rows or columns will be empty once items have been postioned in the cells.
        - Instead ```auto-fit``` collapses those empty rows or columns and stretches your items to fit the size of the container.
    - Use ```minmax``` function to set cell size when container size changes like ```grid-template-columns: 100px minmax(50px, 200px);``` to set 1st column to 100px and 2nd column between 50 and 200px or ```grid-template-columns: repeat(3, minmax(90px, 1fr));```
5. ```grid-gap``` is a shorthand property for grid-row-gap and grid-column-gap from the previous two challenges that's more convenient to use. If grid-gap has one value, it will create a gap between all rows and columns. However, if there are two values, it will use the first one to set the gap between the rows and the second value for the columns.
6. To set the number of columns a item may take use ```grid-column: x / y``` where x and y are the starting and ending lines of the grid. for e.g. ```grid-column: 1 /3 will take the first two columns. Same for rows.
7. In CSS Grid, the content of each item is located in a box which is  referred to as a cell. You can align the content's position within its  cell horizontally using the ```justify-self``` property on a grid item.
    - ```start```: aligns the content at the left of the cell,
    - ```center```: aligns the content in the center of the cell
    - ```end```: aligns the content at the right of the cell.
    - ```stretch``` : default that stretches the content
    - e.g. ```justify-self: center;```
8. Use ```align-self``` to aligns the content vertically within a cell
    -   e.g. ```align-self: center;```
9. Use ```justify-items``` and ```align-items``` to collectively align content in the cells. Same options as #7 and #8.
10. Use group cells together into areas by using ```grid-template-areas``and listing each cell by the group name ans each on each row enclosed in double quotes
    - e.g.  for a 3x3 grid
    ```
    grid-template-areas:
    "header header header"
    "advert content content"
    "footer footer footer"
    ```
11. Once area is set, you can use it to place items in those areas. for e.g.```.item4 {grid-area: header;}```
12. ONe can specify ```grid-area: 1 / 1 / 3 / 4;```instead of #11 which is ```grid-area: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at;```
13. User ```@media``` queries to change dimensions of the grid and placement of items.
```
  .container {
    font-size: 1.5em;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 50px auto 1fr auto;
    grid-gap: 10px;
    grid-template-areas:
      "header"
      "advert"
      "content"
      "footer";
  }

  @media (min-width: 300px){
    .container{
      grid-template-columns: auto 1fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
  }
  ```
  14. You can always create grid within a grid.


