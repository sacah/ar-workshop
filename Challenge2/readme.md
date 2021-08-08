
# Challenge 2 - JavaScript

# Aim
For Challenge 2, to achieve what was shown in the DEMO, we will go through the building blocks for:
- capturing video from your webcam
- passing video through a model that has been trained to recognise faces
- draw an overlay on the video highlighting detected faces 
- saving a detected face with a name 
- recognising single saved face 
- and finally parse multiple faces in one video frame and matching against saved faces to write names on the video feed.

# Browser APIs
### :mag_right: Learning
Browser APIs are built into your web browser, ready-made sets of code building blocks that allow a developer to implement programs that would otherwise be hard or impossible to implement.In this workshop, we will be using

The ```DOM (Document Object Model) API``` allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc. Every time you see a popup window appear on a page, or some new content displayed, that's the DOM in action.
The ```Canvas and WebGL APIs``` allow you to create animated 2D and 3D graphics. 
```Audio and Video APIs``` like HTMLMediaElement and WebRTC allow you to do really interesting things with multimedia, such as play audio and video right in a web page, or grab video from your web camera and display it on someone else's computer.

### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Third party APIs 

Third party APIs are not built into the browser by default, and you generally have to grab their code and information from somewhere on the Web. For example: Twitter API, Google Maps API and the one we are using today is ```face.api```, JavaScript API for Face Recognition in the Browser with tensorflow.js (TensorFlow is used to create large-scale neural networks with many layers and mainly used for deep learning or machine learning problems).
### :books: Dive deeper
https://github.com/justadudewhohacks/face-api.js
https://justadudewhohacks.github.io/face-api.js/docs/index.html

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# setTimeout
### :mag_right: Learning
The setTimeout() method calls a function or evaluates an expression after a specified number of milliseconds. We will using it further in the code.
### :books: Dive deeper
https://www.w3schools.com/jsreF/met_win_settimeout.asp
### :high_brightness: Action
https://codepen.io/sacah/pen/JjNvemK?editors=1010

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Media Stream APIs
### :mag_right: Learning
The ``Navigator`` interface represents the state and the identity of the user agent. ```navigator``` object can be retrieved by read-only window ```navigator``` property.

The ```navigator.mediaDevices``` read-only property returns a MediaDevices object, which provides access to connected media input devices like cameras and microphones, as well as screen sharing (not supported in IE).

The ```MediaDevices.getUserMedia()``` method prompts the user for permission to use a media input which produces a MediaStream with tracks containing the requested types of media. That stream here is a video track produced by a camera pipped to a video element. 

### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia

### :high_brightness: Action
https://codepen.io/sacah/pen/dyWeQjN

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Canvas
### :mag_right: Learning
The HTML <canvas> element is used to draw graphics, on the fly, via JavaScript.

The <canvas> element is only a container for graphics. You must use JavaScript to actually draw the graphics.

### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API

### :high_brightness: Action
https://codepen.io/sacah/pen/poPVQxB

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Capture video ( Camera on)
### :mag_right: Learning
Now the we have learnt how to capture video from the webcam, and draw to a canvas, we combine them.
```setTimeout(function, delay)``` : Executes the function specified by function in delay milliseconds.
```HAVE_ENOUGH_DATA ( value -4) ```: Enough data is available—and the download rate is high enough—that the media can be played through to the end without interruption.

```JS
function isCameraReady() {
  if (video.readyState === video.HAVE_ENOUGH_DATA) {
    printToCanvas();
  } else setTimeout(isCameraReady, 100);
}
```
### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/readyState
  
### :high_brightness: Action
https://codepen.io/sacah/pen/wvdjQRx

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# JavaScript (ES6) features
### :mag_right: Learning
```Async/await``` : syntactical sugar on top of promises. An async function is a function that knows how to expect the possibility of the await keyword being used to invoke asynchronous code.

Invoking an aysnc function returns a promise. Await can be put in front of any async promise-based function to pause your code on that line until the promise fulfills, then return the resulting value.

```Let/Const``` has block scope, variables declared inside a block {} cannot be accessed from outside the block

### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let

### :high_brightness: Action
https://codepen.io/gags1409/pen/WNjaVKJ

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Understanding face-api.js
face-api.js is a JavaScript library that does the heavy lifting required for face detection. It has models included that have already been trained to detect human faces, it does this by detecting various landmarks on our faces, like your eyes and mouth.

face-api.js exposes some APIs we can use to tap into the power it contains.


# Load models 
### :mag_right: Learning
Face-api provides different models but we will use face detection, face landmark and face recognition model for this workshop.

Deep learning neural network models learn to map inputs to outputs given a training dataset of examples. The training process involves finding a set of weights in the network that proves to be good, or good enough, at solving the specific problem.
In another words, the model is the “thing” that is saved after running a machine learning algorithm on training data and represents the rules, numbers, and any other algorithm-specific data structures required to make predictions.


***** (As discussed, CodePens seem to allow external files, though these people will have static-server running, maybe they can start building these examples in the index.html file itself, or make separate .html files for the next few examples. Move code block to Action section and walk them through adding code and what to expect?)

```JS
  await faceapi.loadSsdMobilenetv1Model('/face-api/');
  await faceapi.loadFaceLandmarkModel('/face-api/');
  await faceapi.loadFaceRecognitionModel('/face-api/');
```
***** (mention making function async)

### :books: Dive deeper
https://towardsai.net/p/machine-learning/how-to-build-and-train-your-first-neural-network-9a07d020c4bb
https://deeplizard.com/learn/video/daovGOlMbT4
  
### :high_brightness: Action

Put above code into correct function, change function to async.

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Adding a loading spinner
### :mag_right: Learning
Now that we have asynchronous code, it is useful to display a spinner so users know when loading has finished.

  
### :high_brightness: Action
  Add loader div ( css already in html). You can hide/show loader when needed. Use  .style.display = 'block' | 'none' by fetching element by loader id.
```JS
 <div id="loader"></div>
  
.style.display = 'block';
.style.display = 'none';
```

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# detectSingleFace
### :mag_right: Learning
The networks return the bounding boxes of the face, with the corresponding scores, e.g. the probability of each bounding box showing a face.

```JS
  var singleFaceResultOnLoad;
  singleFaceResultOnLoad = await faceapi.detectSingleFace(video);
  console.log(singleFaceResultOnLoad);
```
Use the DevTools and have a look in the Console as what is contained in singleFaceResultOnLoad.
Other than in the DevTools Console, you won't notice anything happening in the app at this point, but in the next few sections we will use the information in this object to draw landmarks on a face it detected.

### :books: Dive deeper
https://justadudewhohacks.github.io/face-api.js/docs/globals.html#detectsingleface
  
https://justadudewhohacks.github.io/face-api.js/webcam_face_tracking
  
https://github.com/justadudewhohacks/face-api.js/blob/master/examples/examples-browser/views/videoFaceTracking.html
  
https://justadudewhohacks.github.io/face-api.js/docs/index.html
  
### :high_brightness: Action

Add the code from the Learning section to your index.html after the video is ready.
  
:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# withFaceLandmarks() & drawFaceLandmarks
### :mag_right: Learning

***** (Simplify this paragraph)
Next, we want to align the bounding boxes, such that we can extract the images centered at the face for each box before passing them to the face recognition network, as this will make face recognition much more accurate!
For that purpose face-api.js implements a simple CNN, which returns the 68 point face landmarks of a given face image:

```JS
  singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks();
  faceapi.draw.drawFaceLandmarks(canvas, singleFaceResultOnLoad);

  // to further understand it more, we can get positions for 68 point face landmarks and draw boundaries for each
  const context = canvas.getContext("2d");
  const landmarks = singleFaceResultOnLoad.landmarks;
  const jawOutline = landmarks.getJawOutline()
  const nose = landmarks.getNose()
  const mouth = landmarks.getMouth()
  const leftEye = landmarks.getLeftEye()
  const rightEye = landmarks.getRightEye()
  const leftEyeBbrow = landmarks.getLeftEyeBrow()
  const rightEyeBrow = landmarks.getRightEyeBrow()
  faceapi.draw.drawContour(context, jawOutline);
  faceapi.draw.drawContour(context, leftEye);
```

### :books: Dive deeper
https://justadudewhohacks.github.io/face-api.js/docs/index.html#models-face-landmark-detection
  

### :high_brightness: Action

Extend the code to draw more landmarks on the video.

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# How face detection works
### :mag_right: Learning

As we understood the basic of models, there are multiple models we can us for face detection. We are using ``` SSD (Single Shot Multibox Detector)``` as you might have noticed that we loaded in ```Load Models``` step.
  
The networks return the bounding boxes of each face, with their corresponding scores, e.g. the probability of each bounding box showing a face.

**Face Landmark Detection and Face Alignment**

After detection, align the bounding boxes to extract the images centred at the face for each box.
face-api.js implements a simple CNN and  returns the 68 point face landmarks of a given face image.

**Face Recognition**

Feed the extracted and aligned face images into the face recognition network. The network has been trained to learn to map the characteristics of a human face to a ```face descriptor``` (a feature vector with 128 values), which is also oftentimes referred to as face embeddings.

### :books: Dive deeper
https://justadudewhohacks.github.io/face-api.js/docs/index.html#models-face-detection
  
The most accurate face detector is a``` SSD (Single Shot Multibox Detector)```, which is basically a CNN based on MobileNet V1, with some additional box prediction layers stacked on top of the network( use regular convulations which is slower than depthwise seperable convolution)
https://towardsdatascience.com/understanding-ssd-multibox-real-time-object-detection-in-deep-learning-495ef744fab  
  
### :high_brightness: Action
Continue on to the next section.

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# withFaceDescriptor()
### :mag_right: Learning
So far our app will recognise the landmarks of a human face in a video feed. What we'd like it to do is be able to apply a name to a face.

To do this, we need to save the FaceDescriptor against a name, then later we can compare faces we detect in the video feed against saved FaceDescriptors and see if any match.

We add the ```.withFaceDescriptior()``` function to our ```detectSingleFace()``` call to retrieve the FaceDescriptor.

```singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();```

***** (Brief on drawDetections)

### :books: Dive deeper
https://justadudewhohacks.github.io/face-api.js/docs/index.html#usage-displaying-detection-results

### :high_brightness: Action
Modify your code adding in ```.withFaceDescriptors()``` and ```drawDetections()``` to see how it works.

```JS 
  singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();
  faceapi.draw.drawDetections(canvas, singleFaceResultOnLoad);
```

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Event Listeners
### :mag_right: Learning
The addEventListener() method attaches an event handler to the specified element.
  
### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener
  
### :high_brightness: Action
https://codepen.io/sacah/pen/LYyJBRM?editors=1010

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Local storage 
### :mag_right: Learning
The localStorage properties allow to save key/value pairs in a web browser.

The localStorage object stores data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.

### :books: Dive deeper
https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
  
### :high_brightness: Action
https://codepen.io/sacah/pen/yLbxqXz?editors=1010

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Save face descriptor data
### :mag_right: Learning
***** (Rewrite now we've already covered Event listener and Local storage)
EventTarget.addEventListener() : The EventTarget method addEventListener() sets up a function that will be called whenever the specified event is delivered to the target.
localStorage : The localStorage read-only property of the window interface allows you to access a Storage object for the Document's origin; the stored data is saved across browser sessions.

### :books: Dive deeper

### :high_brightness: Action


```JS 
    document.getElementById('add').addEventListener('click', addPerson);
    const faces = {};
    
    function addPerson(event) {
      event.preventDefault();
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      if (faces[name]) {
        alert(`${name} already added`);
        return;
      }
      faces[name] = new faceapi.LabeledFaceDescriptors(name, [singleFaceResultOnLoad.descriptor]);
      console.log("singleFaceResultOnLoad",JSON.stringify(faces));
      localStorage.setItem('faces', JSON.stringify(faces));
      alert(`${name} added successfully`);
      return;
    }
```

#  Add more faces
### :mag_right: Learning

### :books: Dive deeper

### :high_brightness: Action
 const faces = JSON.parse(localStorage.getItem('faces') || '{}');

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Make tabs work 
### :mag_right: Learning

### :books: Dive deeper

### :high_brightness: Action
Add person - for adding face 
Request payment - for recognising and asking for payment
```JS 
var tab = "addPerson";
document.getElementById('requestPaymentTab').addEventListener('click', changeTab);
document.getElementById('addPersonTab').addEventListener('click', changeTab);
function changeTab(ev) {
      clearTimeout(setupCanvas);
      if(ev.target.id == 'requestPaymentTab') {
        tab ='requestPayment';
      } else {
        tab ='addPerson';
      }
      showLoader();
      setupCanvas();
    }

  async function setupCanvas() {
    if (video.readyState === video.HAVE_ENOUGH_DATA) {
        if(tab === 'addPerson') {
          context.clearRect(0, 0, canvas.width, canvas.height);
          singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();
          faceapi.draw.drawDetections(canvas, singleFaceResultOnLoad);
        } else if(tab === 'requestPayment' ) {
            console.log("do something for requestPayment");
        }
        hideLoader();
      } else setTimeout(setupCanvas, 100);
    }

```

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Recognise  single  saved face
### :mag_right: Learning

### :books: Dive deeper

### :high_brightness: Action


--move later
```faceapi.detectAllFaces``` : To detect all face's bounding boxes of an input image/video
Face-api.js implements multiple face detectors for different usecases.

--move later
```How comparison work```
Face descriptor of each extracted face image and compare them with the face descriptors of the reference data. ```Euclidean distance``` is computed between two face descriptors and judge whether two faces are similar based on a threshold value (for 150 x 150 sized face images 0.6 is a good threshold value)

```requestAnimationFrame(callback)```: Tells the browser that you wish to perform an animation and requests that the browser call a specified function to update an animation before the next repaint.
As its async calls , let's put loader to wait for the response
```JS
  async function setupCanvas() {
    if (video.readyState === video.HAVE_ENOUGH_DATA) {
        if(tab === 'addPerson') {
          context.clearRect(0, 0, canvas.width, canvas.height);
          singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();
          console.log(singleFaceResultOnLoad);
          faceapi.draw.drawDetections(canvas, singleFaceResultOnLoad);
        } else if(tab === 'requestPayment' ) {
          requestAnimationFrame(renderFrame);
        }
        hideLoader();
      } else setTimeout(setupCanvas, 100);
    }

    async function renderFrame() {
      await faceID();
    }

  async function faceID() {
      const savedFaceDescriptors = [];
      const requestPeople = [];

      if (Object.keys(faces).length) {
        Object.keys(faces).forEach((face) => {
          savedFaceDescriptors.push(new faceapi.LabeledFaceDescriptors(face, [new Float32Array(faces[face].descriptors[0])]));
        });
      }
      
      let fd =  await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();

      if (savedFaceDescriptors.length) {
        const maxDescriptorDistance = 0.6;
        const faceMatcher = new faceapi.FaceMatcher(savedFaceDescriptors, maxDescriptorDistance);
        context.clearRect(0, 0, canvas.width, canvas.height);
        if(fd){
          const bestMatch = faceMatcher.findBestMatch(fd.descriptor);
          const opts = {
            label: bestMatch.label,
            lineWidth: 2
          };
          const drawBox = new faceapi.draw.DrawBox(fd.alignedRect.box, opts);
          drawBox.draw(canvas);
          if(bestMatch.label!='unknown') {
            document.getElementById('to').value = bestMatch.label;
          }
        }
       
        hideLoader();
      }
      requestAnimationFrame(renderFrame);
    }
```

:heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: :heavy_minus_sign: 

# Recognise  multiple saved face
### :mag_right: Learning
Use ```detectAllFaces``` to detect all faces on video and store it in an array.
and use  ```forEach()``` method to execute a provided function once for each array element.
  
### :books: Dive deeper
https://github.com/justadudewhohacks/face-api.js/blob/master/examples/examples-browser/views/videoFaceTracking.html
https://justadudewhohacks.github.io/face-api.js/docs/globals.html#detectallfaces
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach
  
### :high_brightness: Action

```JS
   async function faceID() {
      const savedFaceDescriptors = [];
      const requestPeople = [];

      if (Object.keys(faces).length) {
        Object.keys(faces).forEach((face) => {
          savedFaceDescriptors.push(new faceapi.LabeledFaceDescriptors(face, [new Float32Array(faces[face].descriptors[0])]));
        });
      }
      
      let detectedFaceDescripters = await faceapi.detectAllFaces(video).withFaceLandmarks().withFaceDescriptors();
      if(detectedFaceDescripters.length) {
        const dims = faceapi.matchDimensions(canvas, video, true);
        detectedFaceDescripters = faceapi.resizeResults(detectedFaceDescripters,dims);
      }
     
      if (savedFaceDescriptors.length) {
        const maxDescriptorDistance = 0.6;
        const faceMatcher = new faceapi.FaceMatcher(savedFaceDescriptors, maxDescriptorDistance);
        context.clearRect(0, 0, canvas.width, canvas.height);

        detectedFaceDescripters.forEach((fd) => {
          const bestMatch = faceMatcher.findBestMatch(fd.descriptor);
          const opts = {
            label: bestMatch.label,
            lineWidth: 2
          };
          const drawBox = new faceapi.draw.DrawBox(fd.alignedRect.box, opts);
            drawBox.draw(canvas);
            if (!requestPeople.includes(bestMatch.label) && bestMatch.label!='unknown') requestPeople.push(bestMatch.label);
            document.getElementById('to').value = requestPeople.join(', ');
        });
        hideLoader();
      }
      requestAnimationFrame(renderFrame);
    }
```
