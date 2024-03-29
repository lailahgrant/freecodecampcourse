#vLearn more about CSS Pseudo selectors by building a Balance Sheet.

Step 5
Below your h1 element, create a div element. Give it an id attribute set to years. You want this particular element to be hidden from screen readers, so give it the aria-hidden attribute set to true.

 <div id="years" aria-hidden="true"></div>


Step 8
HTML tables use the caption element to describe what the table is about. The caption element should always be the first child of a table, but can be positioned with the caption-side CSS property.

Add a caption element to your first table, and give it the text Assets.

          <table>
            <caption>Assets</caption>
          </table>


Step 11
Within each of your new th elements, nest a span element with the class set to sr-only year. Give them the following text (in order): 2019, 2020, and 2021.

Give your third th element the class attribute set to current.

Leave the td element empty. This element exists only to ensure your table has a four-column layout and associate the headers with the correct columns.

       <thead>
              <tr>
                <td></td>
                <th><span class="sr-only year">2019</span></th>
                <th><span class="sr-only year">2020</span></th>
                <th class="current"><span class="sr-only year">2021</span></th>
              </tr>
        </thead>


Step 12
Within your tbody element, add four tr elements. Give the first three a class attribute set to data, and the fourth a class attribute set to total.

            <tbody>
              <tr class="data" ></tr>
              <tr class="data" ></tr>
              <tr class="data" ></tr>
              <tr class="total"></tr>
            </tbody>

Step 13
In your first tr, add a th element with the text Cash This is the cash we currently have on hand.. Wrap all of that text except Cash in a span element with the class set to description.

Following that, add three td elements with the following text (in order): $25, $30, $28. Give the third td element a class attribute set to current.

           <tr class="data">
               <th>Cash <span class="description">This is the cash we currently have on hand.</span></th>
               <td>$25</td>
               <td>$30</td>
               <td class="current">$28</td>
          </tr>


Step 14
In your second tr element, add a th element with the text Checking Our primary transactional account.. Wrap that text, except for Checking , in a span element with the class attribute set to description.

Following that, add three td elements with the following text (in order): $54, $56, $53. Give the third td element a class attribute set to current.

<tr class="data">
                <th>Checking <span class="description">Our primary transactional account.</span></th>
                <td>$54</td>
                <td>$56</td>
                <td class="current">$53</td>
              </tr>


Step 19
Give each th element a span element with the class set to sr-only and the following text, in order: 2019, 2020, and 2021.

<table>
            <caption>Liabilities</caption>
            <thead>
              <tr>
                <td></td>
                <th><span class="sr-only">2019</span></th>
                <th><span class="sr-only">2020</span></th>
                <th><span class="sr-only">2021</span></th>
              </tr>
            </thead>
            <tbody>
            </tbody>
          </table>


Step 20
Within the tbody element, add four tr elements. Give the first three the class attribute set to data, and the fourth the class attribute set to total.

---
        <tbody>
              <tr class="data"></tr>
              <tr class="data"></tr>
              <tr class="data"></tr>
              <tr class="total"></tr>
        </tbody>
---


Step 24
In your fourth tr element, add a th element with the text Total Liabilities. Wrap the text Liabilities in a span element with the class attribute set to sr-only.

Following that, add three td elements with the following text (in order): $750, $600, $475. Give the third td element a class attribute set to current.

<tr class="data">
                <th>Loans <span class="description">The outstanding balance on our startup loan.</span></th>
                <td>$500</td>
                <td>$250</td>
                <td class="current">$0</td>
              </tr>
              <tr class="data">
                <th>Expenses <span class="description">Annual anticipated expenses, such as payroll.</span></th>
                <td>$200</td>
                <td>$300</td>
                <td class="current">$400</td>
              </tr>
              <tr class="data">
                <th>Credit <span class="description">The outstanding balance on our credit card.</span></th>
                <td>$50</td>
                <td>$50</td>
                <td class="current">$75</td>
              </tr>
              <tr class="total">
                <th>Total <span class="sr-only">Liabilities</span></th>
                <td>$750</td>
                <td>$600</td>
                <td class="current">$475</td>
              </tr>


Step 25
For your third table, add a caption with the text Net Worth, and set up a table header and table body.

       <table>
            <caption>Net Worth</caption>
            <thead></thead>
            <tbody></tbody>
       </table>


Step 27
Within the tbody, add a tr with the class set to total. In that, add a th with the text Total Net Worth, and wrap Net Worth in a span with the class set to sr-only.

Then add three td elements, giving the third a class set to current, and giving each the following text: $-171, $136, $334.

<table>
            <caption>Net Worth</caption>
            <thead>
              <tr>
              <td></td>
              <th><span class="sr-only">2019</span></th>
              <th><span class="sr-only">2020</span></th>
              <th><span class="sr-only">2021</span></th>
              </tr>
            </thead>
            <tbody>
              <tr class="total">
                <th>Total <span class="sr-only">Net Worth</span></th>
                <td>$-171</td>
                <td>$136</td>
                <td class="current">$334</td>
              </tr>
            </tbody>
          </table>


Step 28
Time to style your table. Start by resetting the box model. Create an html selector and give it a box-sizing property set to border-box.

html{
  box-sizing:border-box;
}


Step 29
Create a body selector and give it a font-family property set to sans-serif and a color set to #0a0a23.

body{
  font-family:sans-serif;
  color:#0a0a23;
}


Step 31
The CSS clip property is used to define the visible portions of an element. Set the span[class~="sr-only"] selector to have a clip property of rect(1px, 1px, 1px, 1px).

The clip-path property determines the shape the clip property should take. Set the clip-path property to the value of inset(50%), forming the clip-path into a rectangle within the element.

span[class~="sr-only"] {
  border: 0;
  clip-path:inset(50%);
  clip: rect(1px, 1px, 1px, 1px);
}

html {
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  color: #0a0a23;
} 


Step 32
Now you need to size these elements down. Give your span[class~="sr-only"] selector a width and height property set to 1px.

span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  width:1px;
  height:1px;
}


Step 33
To prevent the text content from overflowing, give your span[class~="sr-only"] selector an overflow property set to hidden and a white-space property set to nowrap.

span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  height: 1px;
  width: 1px;
  overflow:hidden;
  white-space:nowrap;
}


Step 34
Finally, you need to take these hidden elements out of the document flow. Give the span[class~="sr-only"] selector a position property set to absolute, a padding property set to 0, and a margin property set to -1px. This will ensure that not only are they no longer visible, but they are not even within the page view.

span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  height: 1px;
  width: 1px;
  overflow: hidden;
  white-space: nowrap;
  position:absolute;
  padding:0;
  margin:-1px;
}


Step 35
Time to style your table heading. Create an h1 selector. Give it a max-width property set to 37.25rem, a margin property set to 0 auto, and a padding property set to 1.5rem 1.25rem.

h1{
  max-width:37.25rem;
  margin:0 auto;
  padding: 1.5rem 1.25rem;
}


Step 36
Target your flex container with an h1 .flex selector. Give it a display property set to flex to enable the flexbox layout. Then set the flex-direction property to column-reverse - this will display the nested elements from bottom to top. Finally, set the gap property to 1rem to create some space between the elements.



Step 38
The :last-of-type pseudo-selector does the exact opposite - it targets the last element that matches the selector. Create an h1 .flex span:last-of-type selector to target the last span in your flex container, and give it a font-size property set to 1.2em to make it look like a header.

h1 .flex span:last-of-type{
  font-size:1.2em;
}


Step 39
You wrapped your table in a section element - now you can style that to give your table a border. Create a section selector, and give it a max-width property set to 40rem for responsive design. Set the margin property to 0 auto to center it, and set the border property to 2px solid #d0d0d5.

section {
  max-width: 40rem;
  margin: 0 auto;
  border: 2px solid #d0d0d5;
}


Step 40
The last part of your table heading is your years. Create a #years selector, and enable flexbox. Justify the content to the end of the flex direction, and make the element sticky. Fix it to the top of its container with top: 0.

#years{
  display:flex;
  justify-content:flex-end;
  position:sticky;
  top:0;
}



Step 44
Style the text within your #years element by creating a #years span[class] selector. The span[class] syntax will target any span element that has a class attribute set, regardless of the attribute's value.

Give your new selector a bold font, a width of 4.5rem, and text aligned to the right.

#years span[class]{
  font-weight:bold;
  width:4.5rem;
  text-align:right;
}


Step 46
Before you start diving in to the table itself, your span elements are currently bolded. Create a span:not(.sr-only) selector and give it a font-weight property set to normal.

The :not() pseudo-selector is used to target all elements that do not match the selector - in this case, any of your span elements that do not have the sr-only class. This ensures that your earlier rules for the span[class~="sr-only"] selector are not overwritten.

span:not(.sr-only){
  font-weight:normal;
}


Step 47
Rather than having to constantly double-check you are not overwriting your earlier properties, you can use the !important keyword to ensure these properties are always applied, regardless of order or specificity.

Give each property in your span[class~="sr-only"] selector an !important keyword. Do not change any of the values.

span[class~="sr-only"] {
  border: 0 !important;
  clip: rect(1px, 1px, 1px, 1px) !important;
  clip-path: inset(50%) !important;
  height: 1px !important;
  width: 1px !important;
  position: absolute !important;
  overflow: hidden !important;
  white-space: nowrap !important;
  padding: 0 !important;
  margin: -1px !important;
}



Step 48
Now that you have added the !important keyword, you can remove the :not(.sr-only) from your span selector.

span {
  font-weight: normal;
}


Step 49
Create a table selector to target your tables. Set the border-collapse property to collapse, which will allow cell borders to collapse into a single border, instead of a border around each cell. Also set the border property to 0 to hide the borders themselves.

table {
  border-collapse: collapse;
  border: 0;
}


Step 50
Ensure your table fills its container with a width property set to 100%, then position it relatively and give it a top margin of 3rem.

table {
  border-collapse: collapse;
  border: 0;
  width:100%;
  position:relative;
  margin-top:3rem;
}


Step 51
Next you need to style your caption elements to look more like headers. Create a table caption selector. Set the text to have a color of #356eaf, a size of 1.3em, and a normal weight.

table caption{
  color:#356eaf;
  font-size:1.3em;
  font-weight:normal;
}


Step 52
Now give the captions an absolute position, and shift them -2.25rem from the top and 0.5rem from the left.

table caption {
  color: #356eaf;
  font-size: 1.3em;
  font-weight: normal;
  position:absolute;
  top: -2.25rem;
  left:0.5rem;
}


Step 54
Now target the th elements within your table body, and give them a width of the entire container, less 12rem.

tbody th{
  width: calc(100% - 12rem);
}


Step 55
The [attribute="value"] selector targets any element that has an attribute with a specific value. Create a tr[class="total"] selector to target specifically your tr elements with the total class. Give it a bottom border of 4px double #0a0a23 and make the font bold.

tr[class="total"]{
  border-bottom: 4px double #0a0a23;
  font-weight:bold;
}


Step 57
The key difference between tr[class="total"] and tr.total is that the first will select tr elements where the only class is total. The second will select tr elements where the class includes total.

In your case, tr.total will work. You can use this selector to target all td elements within your .total rows. Align the text to the right, and give them a padding of 0 0.25rem.

tr.total td {
  text-align: right;
  padding: 0 0.25rem;
}


Step 58
The :nth-of-type() pseudo-selector is used to target specific elements based on their order among siblings of the same type. Use this pseudo-selector to target the third td element within your total table rows. Give it a right padding of 0.5rem.

tr.total td:nth-of-type(3){
  padding:0.5rem;
}


Step 60
Select your td elements with the class value of current, and make the font italic.

td[class="current"]{
  font-style:italic;
}



Step 61
Select the tr elements with the class set to data. Give them a background image of linear-gradient(to bottom, #dfdfe2 1.845rem, white 1.845rem).

tr[class="data"]{
  background-image: linear-gradient(to bottom, #dfdfe2 1.845rem, white 1.845rem);
}


Step 62
Select the th elements within your tr.data elements. Align the text to the left, and give them a top padding of 0.3rem and a left padding of 0.5rem.

tr.data th {
  text-align:left;
  padding: 0.3rem 0.5rem;
}


Step 63
Create a tr.data th .description selector to target the elements with the class set to description that are within your th elements in your .data table rows. Give them a block display, make the text italic with a normal weight, and position them with a padding set to 1rem 0 0.75rem and a right margin of -13.5rem.

tr.data th .description{
  display:block;
  font-weight:normal;
  font-style:italic;
  padding: 1rem 0 0.75rem;
  margin-right:-13.5rem;
}


Step 64
Your span elements now all have more specific styling, which means you can remove your span rule.


Step 65
Your dollar amounts are currently misaligned. Create a selector to target the td elements within your tr.data elements. Vertically align the text to the top, horizontally align the text to the right, and set the padding to 0.3rem 0.25rem 0.

tr.data td{
  vertical-align:top;
  text-align:right;
  padding:0.3rem 0.25rem 0;
}





















