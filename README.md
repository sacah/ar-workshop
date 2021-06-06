# Augmented Reality Workshop

## Pre-work
* Install Node v14+
* Install VS Code
* Install latest Chrome
* Download the ar-workshop (put new repo with no history in) to your laptop
* npm i in ar-workshop folder


## Challenge 1
Focus is on HTML/CSS to make the UI nice and accessible.

## Challenge 2
Focus is on the JavaScript of the app.

## Overview of app
Example of request payment function. Say you're at lunch with friends and want to send them all a payment request. Provided you'd already added your friends, you can just scan all their faces while they are at lunch to add them to a payment request.

For this demo, first load the page, and in the 'Add Person' tab, type the persons name and email. Wait for that person to be the only person detected in the camera and press the 'Add' button.

Now that persons face will be auto detected and named when they are visible.

Click the 'Request payment' button to switch to that tab. When known people are detected, they'll be added to the 'To' field, ready for you to send them a request for payment.

In addition, there is a 'friendAmount' object, with the key being the name you entered, in lower case.
If the amount in this array is negative, the box around the friends face will be red and it will tell you how much they owe.
This amount would populate from an API call in a real system.

## Setup
Start static server
```html
 static-server
```



