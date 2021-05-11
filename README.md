# Augmented Reality Workshop

## Demo1
Uses barcode detection libray to find barcode and put Phone Case $21 over the barcode.
Currently looks for Code 39 barcodes, we should send the code to an API and get title/price back that we then display and cache.

## Demo2
Example of request payment function. Say you're at lunch with friends and want to send them all a payment request. Provided you'd already added your friends, you can just scan all their faces while they are at lunch to add them to a payment request.

For this demo, first load the page, and in the 'Add Person' tab, type the persons name and email. Wait for that person to be the only person detected in the camera and press the 'Add' button.

Now that persons face will be auto detected and named when they are visible.

Click the 'Request payment' button to switch to that tab. When known people are detected, they'll be added to the 'To' field, ready for you to send them a request for payment.

In addition, there is a 'friendAmount' object, with the key being the name you entered, in lower case.
If the amount in this array is negative, the box around the friends face will be red and it will tell you how much they owe.
This amount would populate from an API call in a real system.

### Challenges:
* Students need to figure out the optimum bestMatch.distance, trial and error of taking faces and matching faces
* Implement multiple pictures of face to a better trained model
* Improve the UI (HTML, CSS, little JS)
* Improve the canvas drawing of recognised people, or money owned
