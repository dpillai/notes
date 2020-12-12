1. Use CSS3 ```@media``` query change the presentation of content based on different viewport sizes. The media type should match the devide for the query to be applied. 
For e.g.
```
@media (max-height: 800px) {
    p {
        font-size: 10px;
    }
}
```
2. Make images responsive by
```
.responsive-img {
  max-width: 100%;
  height: auto;
}
```
3. The simplest way to make your images properly appear on High-Resolution Displays, such as the MacBook Pros "retina display" is to define their width and height values as only half of what the original file is. Here is an example of an image that is only using half of the original height and width:
```
<style>
  img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="A most excellent picture">
```
4. Instead of using em or px to size text, you can use viewport units for responsive typography. Viewport units, like percentages, are relative units, but they are based off different items. Viewport units are relative to the viewport dimensions (width or height) of a device, and percentages are relative to the size of the parent container element. The four different viewport units are:
    -   vw (viewport width): 10vw would be 10% of the viewport's width.
    -   vh (viewport height): 3vh would be 3% of the viewport's height.
    -   vmin (viewport minimum): 70vmin would be 70% of the viewport's smaller dimension (height or width).
    -   vmax (viewport maximum): 100vmax would be 100% of the viewport's bigger dimension (height or width).