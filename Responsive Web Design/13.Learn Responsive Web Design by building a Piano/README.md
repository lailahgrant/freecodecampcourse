# Learn Responsive Web Design by building a Piano.


<h5> Responsive Design tells your webpage how it should look on different-sized screens.</h5>

>In this course, you'll use CSS and Responsive Design to code a piano. You'll also learn more about media queries and pseudo selectors.
>
> <img src="./preview.PNG" alt="Preview of the piano we shall create in the course" >

<b>Step 10</b>

>Now that you have reset the html box model, you need to pass that on to the elements within as well. To do this, you can set the box-sizing property to inherit, which will tell the targeted elements to use the same value as the parent element.

>You will also need to target the pseudo-elements, which are special keywords that follow a selector. The two pseudo-elements you will be using are the ::before and ::after pseudo-elements.

>The ::before selector creates a pseudo-element which is the first child of the selected element, while the ::after selector creates a pseudo-element which is the last child of the selected element. These pseudo-elements are often used to create cosmetic content, which you will see later in this project.

For now, create a CSS selector to target all elements with *, and include the pseudo-elements with ::before and ::after. Set the box-sizing property to inherit.

 <pre>
 <code>
*, ::before, ::after {
  box-sizing: inherit;
}
 </pre>
 </code>


<b>Step 11</b>
Now target your #piano element with an id selector. Set background-color property to #00471b, the width property to 992px and the height property to 290px.

<pre>
<code>
#piano {
  background-color : #00471b;
  width:992px;
  height:290px;
}
</code>
</pre>
>

Step 12
Set the margin of the #piano to 80px auto.

<pre>
<code>
 #piano {
  ---
  margin: 80px auto;
}
</pre>
</code>


<b>Step 13</b>
Time to style the keys. Below the #piano rule, target the .keys element with a class selector. Give the new rule a background-color property of #040404, a width property of 949px and a height property of 180px.

<pre>
<code>
.keys{
  background-color : #040404;
  width : 949px;
  height : 180px;
}
</pre>
</code>


Step 14
Give the .keys a padding-left of 2px.

<pre>
<code>
.keys {
  ---
  padding-left : 2px;
}
</pre>
</code>


Step 15
Move the keys into position by adjusting the #piano selector. Set the padding property to 90px 20px 0 20px.

<pre>
<code>
#piano {
  ---
  padding : 90px 20px 0 20px;
}
</pre>
</code>


Step 16
Time to style the keys themselves. Create a class selector for the .key elements. Set the background-color set to the value #ffffff, the position property to relative, the width property to 41px, and the height property to 175px.

<pre>
<code>
.key{
  background-color : #ffffff;
  position : relative;
  width : 41px;
  height : 175px;
}
</pre>
</code>


Step 17
Give the .key a margin of 2px and a float property set to left.

<pre>
<code>
.key {
 ---
  margin: 2px;
  float:left;
}
</pre>
</code>


Step 18
>Now it is time to use the pseudo-selectors you prepared for earlier. To create the black keys, add a new .key.black--key::after selector. This will target the elements with the class key black--key, and select the pseudo-element after these elements in the HTML.

>In the new selector, set the background-color to #1d1e22. Also set the content property to "". This will make the pseudo-elements empty.

>The content property is used to set or override the content of the element. By default, the pseudo-elements created by the ::before and ::after pseudo-selectors are empty, and the elements will not be rendered to the page. Setting the content property to an empty string "" will ensure the element is rendered to the page while still being empty.

- If you would like to experiment, try removing the background-color property and setting different values for the content property, such as "♥". Remember to undo these changes when you are done so the tests pass.

<pre>
<code>
.key.black--key::after{
  background-color : #1d1e22;
  content:"";
}
</pre>
</code>


Step 19
Give the .key.black--key::after a position property set to absolute and a left property set to -18px.

<pre>
<code>
.key.black--key::after {
  ---
  position:absolute;
  left:-18px;
}
</pre>
</code>


Step 20
For the .key.black--key::after, set the width to 32px and the height to 100px.

<pre>
<code>
.key.black--key::after {
  ---
  width:32px;
  height:100px;
}
</pre>
</code>


Step 21
The piano needs the freeCodeCamp logo to make it official.

Add an img element before your .keys element. Give the img a class of logo, and set the src to https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg. Give it an alt text of freeCodeCamp Logo.


> <div id="piano">
>      <img class="logo" src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" alt="freeCodeCamp Logo" />
> ---
> </div>


Step 22
Start styling the logo by creating a .logo selector. Set the width to 200px, a position of absolute and a top set to 23px.
<pre>
<code>
.logo{
  width:200px;
  position:absolute;
  top:23px;
}
</pre>
</code>


Step 23
The img element needs its parent to have a position set as a point of reference. Set the position of the #piano selector to relative.
<pre>
<code>
#piano {
  ---
  position:relative;
}
</pre>
</code>


Step 24
To smooth the sharp edges of the piano and keys, start by giving the #piano a border-radius of 10px.
<pre>
<code>
#piano {
  ---
  border-radius:10px;
}
</pre>
</code>


Step 25
Give the .key selector a border-radius value of 0 0 3px 3px.
<pre>
<code>
.key {
  ---
  border-radius : 0 0 3px 3px;
}
</pre>
</code>


Step 26
Give the .key.black--key::after selector a border-radius of 0 0 3px 3px to match the keys.
<pre>
<code>
.key.black--key::after {
  ---
  border-radius: 0 0 3px 3px;
}
</pre>
</code>


Step 27
The @media at-rule, also known as a media query, is used to conditionally apply CSS. Media queries are commonly used to apply CSS based on the viewport width using the max-width and min-width properties.

In the below example the padding is applied to the .card class when the viewport is 960px wide and below.

>@media (max-width: 960px) {
>  .card {
>    padding: 2rem;
>  }
>}

Add a media query that will be applied when the viewport is 768px wide and below.
<pre>
<code>
@media (max-width: 768px){
  
}
</pre>
</code>

Step 28
Add a new #piano selector within your @media query, and set the width to 358px.

<pre>
<code>
@media (max-width: 768px) {
#piano{
  width:358px;
}
}
</pre>
</code>


Step 29
Within the @media query, add a .keys selector and set the width to 318px.
<pre>
<code>
@media (max-width: 768px) {
  #piano {
    width: 358px;
  }
  .keys{
    width:318px;
  }
}
</pre>
</code>


Step 30
Now add a .logo selector to the @media query, and set the width property to 150px.
<pre>
<code>
@media (max-width: 768px) {
  ---
  .logo{
    width:150px;
  }
}
</pre>
</code>


Step 31
You might have noticed the keys collapse when the browser window is smaller than 768px. Set overflow to hidden in the first .keys selector, to take care of this issue. This property will hide any element that is pushed outside the set width value of .keys.

<pre>
<code>
.keys {
  ---
  overflow:hidden;
}
</pre>
</code>


Step 32
Logical operators can be used to construct more complex media queries. The and logical operator is used to query two media conditions.

For example, a media query that targets a display width between 500px and 1000px would be:

>@media (min-width: 500px) and (max-width: 1000px){
>
>}

Add another @media rule to apply if the browser window is wider than 769px but smaller than 1199px.
<pre>
<code>
@media (min-width: 769px) and (max-width: 1199px){
  
}
</pre>
</code>


Step 33
For the new @media rule, set the width of the #piano to 675px and the width of the .keys to 633px.

With that, your piano is complete!

<pre>
<code>
@media (max-width: 1199px) and (min-width: 769px) {
#piano{
  width:675px;
}

.keys{
  width:633px;
}
}
</pre>
</code>
