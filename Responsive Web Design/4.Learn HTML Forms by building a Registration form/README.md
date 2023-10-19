# Learn HTML forms by building a Registration form.
> You can use HTML forms to collect information from people who visit your webpage.

> In this course, you'll learn HTML forms by building a signup page. You'll learn how to control what types of data people can type into your form, and some new CSS tools for styling your page.

<hr>

1) The method attribute specifies how to send form-data to the URL specified in the action attribute. The form-data can be sent via a GET request as URL parameters (with method="get") or via a POST request as data in the request body (with method="post").
> Set the method attribute to send your form data via a POST request.

index.html

>
> action='https://register-demo.freecodecamp.org' method='post'> in a form tag.

<hr style="border: 1px dashed black">

2) The rem unit stands for root em, and is relative to the font size of the html element.

- As label elements are inline by default, they are all displayed side by side on the same line, making their text hard to read. To make them appear on separate lines, add display: block to the label element, and add a margin of 0.5rem 0, to separate them from each other.

<hr style="border: 1px dotted black">


3) Following accessibility best practices, link the input elements and the label elements together using the for attribute.

Use first-name, last-name, email, and new-password as values for the respective id attributes.

<hr style="border: 1px groove black">


4) Specifying the type attribute of a form element is important for the browser to know what kind of data it should expect. If the type is not specified, the browser will default to text.

Give the first two input elements a type attribute of text, the third a type attribute of email, and the fourth a type attribute of password.

The email type only allows emails with a @ and a . in the domain. The password type obscures the input, and warns if the site does not use HTTPS.

<hr style="border: 1px double  black">


5) Certain type attribute values come with built-in form validation. For example, type="email" requires that the value be a valid email address.

Add custom validation to the password input element, by adding a minlength attribute with a value of 8. Doing so prevents inputs of less than 8 characters being submitted.
 minlength="8" in the input tag

<hr style="border: 1px ridge  black">


6) With type="password" you can use the pattern attribute to define a regular expression that the password must match to be considered valid.

Add a pattern attribute to the password input element to require the input match: [a-z0-5]{8,}

The above is a regular expression which matches eight or more lowercase letters or the digits 0 to 5. Then, remove the minlength attribute, and try it out. 
 pattern="[a-z0-5]{8,}" in the input tag


7) You only want one radio input to be selectable at a time. However, the form does not know the radio inputs are related.

To relate the radio inputs, give them the same name attribute with a value of account-type. Now, it is not possible to select both radio inputs at the same time.


8) Currently when someone submit the form, they can submit it without checking the radio inputs. Although you had used required attribute to indicate the the input is required previously, this can't work in this case, because adding required to both inputs, will convey the wrong information to the form users.

To solve this, you can provide context of what is needed by adding **legend** element below the second fieldset with text Account type (required), then add **checked** attribute to the Personal input to make sure that the form is submitted with the required data in it.


9) Follow accessibility best practices by linking the input elements and the label elements in the second fieldset.

Use personal-account, and business-account as values for the respective id attributes, with the for attribute to the respective label tags.


10) You need to confirm that the user has read the terms and conditions.

Add label element after the third fieldset, and a input element with type attribute of checkbox inside the newly added label element. Make this input element required because users should not sign up without reading the terms and conditions.

Don't forget to add an id attribute of terms-and-conditions for accessibility.

11) Moving on to the final fieldset. What if you wanted to allow a user to upload a profile picture?

Well, the *input* type **file** allows just that. Add a label with the text Upload a profile picture: , and nest an input accepting a file upload.


12) Add another label after the first, with the text Input your age (years): . Then, nest an input with the type of number.

Next, add a min attribute to the input with a value of 13 because users under the age of 13 should not register. Also, users probably will not be over the age of 120; add a max attribute with a value of 120.

Now, if someone tries to submit the form with values outside of the range, a warning will appear, and the form will not submit. Give it a try.