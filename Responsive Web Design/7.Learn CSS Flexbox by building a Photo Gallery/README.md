# Learn CSS Flexbox by building a Photo Gallery

> Flexbox helps you design your webpage so that it looks good on any screen size.
>
>In this course, you'll use Flexbox to build a responsive photo gallery webpage.

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

<hr>

Step 14
*Flexbox* is a one-dimensional CSS layout that can control the way items are spaced out and aligned within a container.

To use it, give an element a display property of flex. This will make the element a flex container. Any direct children of a flex container are called flex items.

Create a .gallery selector and make it a flex container.

.gallery{
  display:flex;
}


Step 15
Flexbox has a main and cross axis. The main axis is defined by the flex-direction property, which has four possible values:

row (default): horizontal axis with flex items from left to right
row-reverse: horizontal axis with flex items from right to left
column: vertical axis with flex items from top to bottom
column-reverse: vertical axis with flex items from bottom to top
Note: The axes and directions will be different depending on the text direction. The values shown are for a left-to-right text direction.

Try the different values to see how they affect the layout.

When you are done, set an explicit flex-direction of row on the .gallery element.

.gallery{
  display:flex;
  flex-direction:row;
}


Step 16
The flex-wrap property determines how your flex items behave when the flex container is too small. Setting it to wrap will allow the items to wrap to the next row or column. nowrap (default) will prevent your items from wrapping and shrink them if needed.

Make it so your flex items wrap to the next row when they run out of space.

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}


Step 17
The justify-content property determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

Give your .gallery selector a justify-content property with center as the value.

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content:center;
}


Step 18
The align-items property positions the flex content along the cross axis. In this case, with your *flex-direction* set to *row*, your *cross axis* would be *vertical*.

To vertically center your images, give your .gallery selector an align-items property with center as the value.

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items:center;
}


Step 19
Give your .gallery selector a padding property set to 20px 10px to create some space around the container.

Then, give it a max-width of 1400px and add a margin of 0 auto to center it.

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding:20px 10px;
  max-width:1400px;
  margin:0 auto;

}



Step 20
> Notice how some of your images have become distorted. This is because the images have different aspect ratios. Rather than setting each aspect ratio individually, you can use the *object-fit* property to determine how images should behave.

Give your *.gallery img* selector the *object-fit* property and set it to *cover*. This will tell the image to fill the img container while maintaining aspect ratio, resulting in cropping to fit.

.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
  object-fit:cover;
}



Step 21
Your images need some space between them.

The *gap* CSS shorthand property sets the gaps, also known as gutters, between rows and columns. The gap property and its row-gap and column-gap sub-properties provide this functionality for flex, grid, and multi-column layout. You apply the property to the container element.

Give your .gallery flex container a gap property with 16px as the value.

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  max-width: 1400px;
  margin: 0 auto;
  padding: 20px 10px;
  gap:16px;
}


Step 22
Smooth out your images a bit by giving the .gallery img selector a border-radius property with 10px set as the value.

.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
  object-fit: cover;
  border-radius:10px;
}



Step 23
The ::after pseudo-element creates an element that is the last child of the selected element. You can use it to add an empty element after the last image. If you give it the same width as the images it will push the last image to the left when the gallery is in a two-column layout. Right now, it is in the center because you set justify-content: center on the flex container.

Example:
<code>
.container::after {
  content: "";
  width: 860px;
}
</code>
Create a new selector using an ::after pseudo-element on the .gallery element. Add a content property set to an empty string "" and 350px set for the width property.

.gallery::after{
  content:"";
  width:350px;
}



Step 24
The alt image attribute should describe the image content. Screen readers announce the alternative text in place of images. If the image can't be loaded, this text is presented in place of the image.

To complete the project, add an alt attribute to all nine of your cat images to describe them. Use a value at least five characters long for each.

<img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg" alt="eyes closed brown and white cat">
<img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg" alt="cat lying on the ground in a playful way">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg" alt="sweet little alert guy">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg" alt="well covered cat sleeping in bed">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg" alt="all white with big water-green eyes">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg" alt="two brown cats">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg" alt="awake covered cat">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg" alt="beautiful orange little cat">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg" alt="one black and partial white cat">



































































