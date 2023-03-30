# Body part segmentation using pre trained model in TensorFlow.js

## What can this demo do?

This demo shows how we can use a pre made machine learning solution to recognize pixels in an image that belong to a human body and even what sub parts of the body they belong to (e.g. an arm, leg, head etc). We can get data for all pixels in the image which is super useful as then you could do things like blur the background to get a cool depth of field effect, or maybe you want to blur just the face to retain user privacy. The possibilities are endless.


## What's in all the files?

### ← index.html

We simply have some script tags in our HTML to grab the latest version of TensorFlow.js and the machine learning model class that can take image data as input and output predictions for any pixels it associates with being part of a human body.

In this case we simply reference the following to bring in TensorFlow.js:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs/dist/tf.min.js" type="text/javascript"></script>
```

However, if you want to pull in a particular version of TensorFlow.js you can do so like this:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.4.0/dist/tf.min.js" type="text/javascript"></script>
```

Finally you will see that we pull in the machine learning model class we later use in script.js like this:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/body-pix@2.0"></script>
```

### ← style.css

Nothing to see here. Just styles to make the demo look prettier. You can use or ignore these as you please.

### ← script.js

This file shows the demo code you need to write in JavaScript to interact with the BodyPix class we imported in the HTML. This is where the magic happens. We can pass data to the class and then retrive predictions on what it thinks it saw in the image which we can then use to make a decision. The file is well commented so do read the comments to learn more. Demos are provided for images in the DOM and also live webcam stream classification.

---
