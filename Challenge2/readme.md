
# Challenge 2 - JavaScript

* JavaScipt overview
* Initiate Javascript


## JavaScipt overview
JavaScript is a scripting language that  allows you to implement complex features on web pages. It makes HTML pages dynamic. Include JavaScript by <script> tags in HTML pages
We are using ES6 in this workshop.
```html
<script></script>
```

### Initiate Javascript
A JavaScript function is a block of code designed to perform a particular task.Its executed when "something" invokes it (calls it).
```html
<script>
    function init() {
        console.log("Lets start");
    }
    init();
</script>   
```

## Browser APIs
Browser APIs are built into your web browser, ready-made sets of code building blocks that allow a developer to implement programs that would otherwise be hard or impossible to implement.In this workshop, we will be using

The ```DOM (Document Object Model) API``` allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc. Every time you see a popup window appear on a page, or some new content displayed (as we saw above in our simple demo) for example, that's the DOM in action.
The ```Canvas and WebGL APIs``` allow you to create animated 2D and 3D graphics. People are doing some amazing things using these web technologies —see Chrome Experiments and webglsamples.
```Audio and Video APIs``` like HTMLMediaElement and WebRTC allow you to do really interesting things with multimedia, such as play audio and video right in a web page, or grab video from your web camera and display it on someone else's computer (try our simple Snapshot demo to get the idea).

## Third party APIs 
Third party APIs are not built into the browser by default, and you generally have to grab their code and information from somewhere on the Web. For example: Twitter API,Google Maps API  and the one we are using today is ```face.api```( JavaScript API for Face Recognition in the Browser with tensorflow.js).

```html
<script src="/face-api/face-api.min.js" type="text/javascript"></script>
```

### Capture video ( Camera on)
A variable declared outside a function, becomes GLOBAL.
Media Stream APIs
The ``Navigator`` interface represents the state and the identity of the user agent. ```navigator``` object can be retrieved by read-only window ```navigator``` property.
The ```Navigator.mediaDevices``` read-only property returns a MediaDevices object, which provides access to connected media input devices like cameras and microphones, as well as screen sharing (not supported in IE).
The ```MediaDevices.getUserMedia()``` method prompts the user for permission to use a media input which produces a MediaStream with tracks containing the requested types of media. That stream here is a video track produced by a camera.     

```html
var video = document.getElementById("video"); //Global variable
function init() {
      navigator.mediaDevices.getUserMedia({ audio: false, video: true, video: { width: 480, height: 360 }}).then((stream) => {
        video.srcObject = stream;
        //setupCanvas();
      }).catch(function(err) {
        /* handle the error */
        console.log("error in capturing video");
    });
}
```


### More ES6 featues
```Aync/await``` : ES6 recent additions , syntactic sugar on top of promises. An async function is a function that knows how to expect the possibility of the await keyword being used to invoke asynchronous code.
Invoking aysnc function returns a promise. Await can be put in front of any async promise-based function to pause your code on that line until the promise fulfills, then return the resulting value.

Before ES2015, JavaScript had only two types of scope: Global Scope and Function Scope
```Let/Const``` has block scope, Variables declared inside a block {} cannot be accessed from outside the block

### Understanding face-api.js
```faceapi.detectAllFaces``` : To detect all face's bounding boxes of an input image/video
Face-api.js implements multiple face detectors for different usecases.
```Face Detection```
The most accurate face detector is a``` SSD (Single Shot Multibox Detector)```, which is basically a CNN based on MobileNet V1, with some additional box prediction layers stacked on top of the network( use regular convulations which is slower than depthwise seperable convolution)

The networks return the bounding boxes of each face, with their corresponding scores, e.g. the probability of each bounding box showing a face.

```Face Landmark Detection and Face Alignment```
After detection, align the bounding boxes to extract the images centred at the face for each box.
face-api.js implements a simple CNN and  returns the 68 point face landmarks of a given face image.

```Face Recognition``` 
Feed the extracted and aligned face images into the face recognition network. The network has been trained to learn to map the characteristics of a human face to a ```face descriptor``` (a feature vector with 128 values), which is also oftentimes referred to as face embeddings.

```How comparison work```
Face descriptor of each extracted face image and compare them with the face descriptors of the reference data. ```Euclidean distance``` is computed between two face descriptors and judge whether two faces are similar based on a threshold value (for 150 x 150 sized face images 0.6 is a good threshold value)

```Load models```
Face-api provides different models but we will use face detection, face landmark and face recognition model for this workshop.

```html
    //put async and load models in init function
     async function init() {
      await faceapi.loadSsdMobilenetv1Model('/face-api/');
      await faceapi.loadFaceLandmarkModel('/face-api/');
      await faceapi.loadFaceRecognitionModel('/face-api/');
      navigator.mediaDevices.getUserMedia({ audio: false, video: true, video: { width: 480, height: 360 }}).then((stream) => {
        video.srcObject = stream;
        //setupCanvas();
      });
    }
    
```

### Setup Canvas and detect single face 
Detect single face , return landmarks to face decriptor.
```getElementById()```:  method returns the element that has the ID attribute with the specified value
```setTimeout(function, delay)``` : Executes the function specified by function in delay milliseconds.
```HAVE_ENOUGH_DATA ( value -4) ```: Enough data is available—and the download rate is high enough—that the media can be played through to the end without interruption.
```requestAnimationFrame(callback)```: Tells the browser that you wish to perform an animation and requests that the browser call a specified function to update an animation before the next repaint.
As its async calls , let's put loader to wait for the response
```html
    var canvas = document.getElementById("canvas");
    var singleFaceResultOnLoad;

    function setupCanvas() {
    if (video.readyState === video.HAVE_ENOUGH_DATA) {
        singleFaceResultOnLoad = await faceapi.detectSingleFace(video).withFaceLandmarks().withFaceDescriptor();
        faceapi.draw.drawDetections(canvas, singleFaceResultOnLoad);
        hideLoader();
      } else setTimeout(setupCanvas, 100);
    }
    // uncomment setupCanvas();

    //put loader 
     function showLoader(){
      document.getElementById("loader").style.display ='block';
    }
    function hideLoader(){
      document.getElementById("loader").style.display ='none';
    }

```

### Add Person
EventTarget.addEventListener() : The EventTarget method addEventListener() sets up a function that will be called whenever the specified event is delivered to the target.
```html 
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

### Detect the already saved face 

```html
    //fetch data from localstorage 
    const faces = JSON.parse(localStorage.getItem('faces') || '{}');

    var context = canvas.getContext("2d");
    
    // change setCanvas
    function setupCanvas() {
        if (video.readyState === video.HAVE_ENOUGH_DATA) {
        requestAnimationFrame(renderFrame);
       } else setTimeout(setupCanvas, 100);
    }

    async function renderFrame() {
      await faceID();
    }

     async function faceID() {
      const faceDescriptors = [];
      if (Object.keys(faces).length) {
        Object.keys(faces).forEach((face) => {
          faceDescriptors.push(new faceapi.LabeledFaceDescriptors(face, [new Float32Array(faces[face].descriptors[0])]));
        });
      }
      
      let faceLandmarks = await faceapi.detectAllFaces(video).withFaceLandmarks().withFaceDescriptors();

      if (faceDescriptors.length) {
        const faceMatcher = new faceapi.FaceMatcher(faceDescriptors);
        context.clearRect(0, 0, canvas.width, canvas.height);
        faceLandmarks.forEach((fd) => {
          const bestMatch = faceMatcher.findBestMatch(fd.descriptor);
          const opts = {
            label: bestMatch.label,
            lineWidth: 2
          };
          if (bestMatch.distance <= 0.5) {
            const drawBox = new faceapi.draw.DrawBox(fd.alignedRect.box, opts);
            drawBox.draw(canvas);
            if (document.getElementById('requestPaymentTab').checked) {
              if (!requestPeople.includes(bestMatch.label)) requestPeople.push(bestMatch.label);
              document.getElementById('to').value = requestPeople.join(', ');
            }
          } else {
            faceapi.draw.drawFaceLandmarks(canvas, fd.landmarks);
          }
        });
      }
      requestAnimationFrame(renderFrame);
    }
```
