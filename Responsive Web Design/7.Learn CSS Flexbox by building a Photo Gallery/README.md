# Learn CSS Flexbox by building a Photo Gallery

### box-sizing approach

index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link rel="stylesheet" href="./styles.css">
  </head>
  <body>
    <header class="header">
      <h1>css flexbox photo gallery</h1>
    </header>
    <div class="gallery">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg">
    </div>
  </body>
</html>

styles.css

/*
*Step 8
Notice how the blue image border extends beyond the red gallery border. This is due to the way browsers calculate the size of container elements.

The box-sizing property is used to set this behavior. By default, the content-box model is used. With this model, when an element has a specific width, that width is calculated based only on the element's content. Padding and border values get added to the total width, so the element grows to accommodate these values.

Try setting box-sizing to content-box explicitly, with the global * selector. At this point, you will not see any changes, because you are using the default value.
 */

* {
    /*box-sizing:content-box;*/ /**the default */
  box-sizing: border-box;
}

/*
* Step 9
The border-box sizing model does the opposite of content-box. The total width of the element, including padding and border, will be the explicit width set. The content of the element will shrink to make room for the padding and border.

Change the box-sizing property to border-box. Notice how your blue image borders now fit within your red gallery border.

 */

.gallery {
  border: 5px solid red;
  width: 50%;
}

img {
  width: 100%;
  border: 5px solid blue;
  padding: 5px;
}

<hr>

Step 11
Now your images are too big.

Create a .gallery img selector to target them. Give them all a width of 100% and a max-width of 350px.

Also set the height property to 300px to keep your images a uniform size.
.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
}


Step 12
Remove the margin from your body element, set the font-family to sans-serif, and give it a background-color of #f5f6f7 as the value.
* {
  box-sizing: border-box;
}

body{
  margin:0;
  font-family: sans-serif;
  background-color: #f5f6f7;
}


Step 13
Align your .header text in the center. Make the text uppercase using the text-transform property with uppercase as the value.

Give it a padding of 32px on all sides. Set the background to #0a0a23 and the text to #fff as the color values.

Add a border-bottom with 4px solid #fdb347 as the value.
.header{
  text-align:center;
  text-transform: uppercase;
  padding:32px;
  background-color:#0a0a23;
  color:#fff;
  border-bottom: 4px solid #fdb347;
}










