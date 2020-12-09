### Applied Accessibility
1. Alt Attribute
    -   Using Alt attribute is mandatory for img elements in HTML5.
    -   Allows screen readers to pick up on it
    -   helps search engines to catalog
2. Heading
    -   Use 1 and only 1 H1 tag
    -   Use headings to semantically structure the content
3. Use html 5 elements like main, header, footer, article, section and nav to give semantic meaning
4. audio element to embed media files
```
<audio controls>
    <source src="" type="audio/mpeg"> 
</audio>
```
5. figure element 
```
<figure>
    <img src=""> <br>
    <figcaption>text</figcaption
</figure>
```
6. fieldset element to group radio options together
```
<fieldset>
    <legend>caption</legend>
    <input type="radio" id="1" value="1" name="1>
    <label for="1">Choice 1</label>
</fieldset>
```
7. input type=date. For older browsers use label to ask for the right format
```
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```
8. Use ```datetime``` atribute for ```time`` element to stadardize time
```
<p>text<time datetime="2020-12-20">Thursday Set 15th </time></p>
``` 
9. Use CSS to position screen reader only elements off the visual are by
```
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```
10. Give Links Meaning by Using Descriptive Link Text
11. Use accesskey attribute for keyboarde only users
```
<h2><a id="first" href="#" accesskey="g">The Garfield Files: Lasagna as Training Fuel?</a></h2>
```
12. The HTML tabindex attribute has three distinct functions relating to an element's keyboard focus. When it's on a tag, it indicates that element can be focused on. The value (an integer that's positive, negative, or zero) determines the behavior.
    -   Can be used w/ pseudo class like :focus when the tabindex is set
    ```
    <div tabindex="0">I need keyboard focus!</div>

    <input type="search" name="search" id="search" tabindex="1">
    <input type="submit" name="submit" value="Submit" id="submit" tabindex="2">
    ```