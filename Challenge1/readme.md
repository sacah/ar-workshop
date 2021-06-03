
# Challenge 1 - HTML/CSS

* HTML, overview
* INPUTs, types and functionality of radios
* LABELs, how they interact with INPUTs
* CSS, overview
* CSS, .class selector
* CSS, label selector
* CSS, input[name='tab'] selector
* CSS, > child selector
* CSS, + sibling selector
* CSS, input:checked selector
* CSS, label:hover selector
* CSS, display: flex
* CSS, display: grid, grid-column
* CSS, animation

## HTML overview
HTML (HyperText Markup Language) is used to structure and give meaning to content on web pages. Below is a simple example of a basic HTML file.
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Hello world</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
  <p>Hello world!</p>
</body>
</html>
```

Tags are the building blocks of HTML files, a tag is defined between the <>, so in the above example we have the following tags: ```html```, ```head```, ```meta```, ```title```, ```body``` & ```p```. Are you able to find each of these tags?

You might notice that many of these tags appear twice, the first like ```<title>``` and the second like ```</title>```, the first one is the opening tag, the second one, with the / is the closing tag. Any text that appears between the opening and closing tags is considered the tags value, in the instance of the ```<title>``` tag, this text will become the title of the page.

Some of the tags in our example also have attributes. Attributes are additional properties assigned to that tag. ```<html lang="en">```, here we open a HTML tag, and add an attribute lang, which we assign the value en. This attribute sets the language of this HTML file. There are many possible attributes on each html tag, you can look each tag up on the [HTML - MDN (Mozilla Developers Network)](https://developer.mozilla.org/en-US/docs/Web/HTML) to dig deeper.


## INPUTs
The ```<input>``` HTML tag is an element that has a number of different types, all focused around input from the user in some way.

For the ```<input>``` tag, type is an attribute, type can have many different values, to see more in-depth information, look at [Input - MDN (Mozilla Developers Network)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Input).

Here are a few common values for the attribute type
```html
<input type="text" value="test">
<input type="radio" name="question">
<input type="radio" name="question">
<input type="password" value="test">
```
See these in action at https://codepen.io/sacah/pen/RwpQdPN

### type="radio"
In the above example of 2 radio inputs, notice how the name attribute has the same value. This forms a group, and only allows 1 to be selected at a time. If you click on one ofthe radio inputs above, you'll notice it becomes selected. If you then click on the other radio input, the previous one becomes unselected and the new one becomes selected. This is important behaviour that we can use later.


## LABELs
The ```<label>``` HTML tag seems simple, just displaying the text from the tags value. However a LABEL allows you to link this text to an INPUT. You notice in our INPUT examples above, there is nothing to tell you what the field is, the first INPUT is just a text box, how do you know what you should enter?

```html
<label for="firstname">First name</label>
<input type="text" id="firstname">
```
See these in action at https://codepen.io/sacah/pen/RwpQdPN

Now with a label, we can identify what information the INPUT wants us to enter. An important behaviour of LABELs is when you click on the label text, you will notice that it directs your focus to the INPUT it is linked with.

## CSS overview
CSS (Cascading Style Sheets) is used to define the layout and style of HTML tags. CSS can be entered as the value of a ```<style>``` HTML tag. Here is an example that styles all the text on a page to be blue.
```HTML
<style>
* {
    color: blue;
}
</style>
```

In the example above, ```*``` is the selector, and ```color``` is the property and ```blue``` is the property value. You can have multiple properties per selector, and you can even chain multiple selectors to assign them the same properties.
```CSS
input,
label {
    color: blue;
    font-weight: bold;
    background-color: black;
}
```
In the above example, we've said find any HTML ```input``` or ```label``` tags, and style them so their text color is blue, their text is bold and the background color is black.

We will cover different selectors and some properties below, though to really dig deeper into CSS, look at [CSS - MDN (Mozilla Developers Network)](https://developer.mozilla.org/en-US/docs/Web/CSS).

## Class selector
