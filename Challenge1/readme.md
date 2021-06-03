
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
HTML is a scripting language, it's written in plain text and interprited by the browser. Here is a simple example HTML file.
```
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

Tags are the building blocks of HTML files, a tag is defined between the <>, so in the above example we have the following tags: html, head, meta, title, body & p. Are you able to find each of these tags?

You might notice that many of these tags appear twice, the first like \<title> and the second like \</title>, the first one is the opening tag, the second one, with the / is the closing tag. Any text that appears between the opening and closing tags is considered the tags value, in the instance of the \<title> tag, this text will become the title of the page.

Some of the tags in our example also have attributes. Attributes are additional properties assigned to that tag. \<html lang="en">, here we open a HTML tag, and add an attribute lang, which we assign the value en. This attribute sets the language of this HTML file. There are many possible attributes on each html tag, you can look each tag up on the [MDN (Mozilla Developers Network)](https://developer.mozilla.org/en-US/docs/Web/HTML) to dig deeper.


## INPUTs
The \<input> HTML tag is an element that has a number of different types, all focused around input from the user in some way.

For the \<input> tag, type is an attribute, type can have many different values, to see more in-depth information, look at [Input - MDN (Mozilla Developers Network)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Input).

Here are a few common values for the attribute type
```
<input type="text" value="test">
```
<input type="text" value="test">

```
<input type="radio" name="question">
<input type="radio" name="question">
```
<input type="radio" name="question">
<input type="radio" name="question">

```
<input type="password" value="test">
```
<input type="password" value="test">


### type="radio"
In the above example of 2 radio inputs, notice how the name attribute has the same value. This forms a group, and only allows 1 to be selected at a time. If you click on one ofthe radio inputs above, you'll notice it becomes selected. If you then click on the other radio input, the previous one becomes unselected and the new one becomes selected. This is important behaviour that we can use later.


## LABELs
The \<label> HTML tag seems simple, just displaying the text from the tags value. However a LABEL allows you to link this text to an INPUT. You notice in our INPUT examples above, there is nothing to tell you what the field is, the first INPUT is just a text box, how do you know what you should enter?

```
<label for="firstname">First name</label>
<input type="text" id="firstname">
```
<label for="firstname">First name</label>
<input type="text" id="firstname">

Now with a label, we can identify what information the INPUT wants us to enter. An important behaviour of LABELs is when you click on the label, you will notice that it directs your focus to the INPUT it is linked with.
