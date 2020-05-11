#Face Detection by RK University
Simple python code for face detection.

Step 1 : download python and install it.
<a href="https://www.python.org/downloads/">Click here</a>

step 2 : install openCV library for that
<ol>
  <li>Open command promt</li>
  <li>type : <b>pip install opencv-python</b></li>
  <li><a href="https://github.com/sejpalsinh/facedetection">click here</a></li>
  <li>Click on Clon or Download -> Download Zip</li>
  <li>Extract that zip</li>
  <li>Now open command promt/CMD and using command goto that folder location</li>
  <li>Now Type : <b>python facedetect.py</b></li>
  <li>Press 'q' for turn off</li>
</ol>  

<h2><b>Explanation for code</b></h2>
<h4>use for adding open-cv library</h4>
<code>import cv2</code>  
<h4>Use for adding model file</h4>
<code>face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml') </code> 
<h4>To get access your camera</h4>
<code>cap = cv2.VideoCapture(0)</code> 
<h4>It will get fram from your camera stream</h4>
<code>_, img = cap.read()</code> 
<h4>Convert normal frame to gray image frame</h4>
<code>gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)</code> 
<h4>Now try to match face shape from loaded xml file</h4>
<code>faces = face_cascade.detectMultiScale(gray, 1.1, 4)</code>
<h4>Draw the rectangle around each face when face detected</h4>
<code>for (x, y, w, h) in faces:</code>
<code>&nbsp&nbsp&nbsp&nbspcv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)</code>
<h4>Display image</h4>
<code>cv2.imshow('img', img)</code>
<h4>Stop if 'q' key is pressed</h4>
<code>if cv2.waitKey(1) & 0xFF == ord('q'):</code>
<h4>After using camera we have to make it free</h4>
<code>cap.release()</code>
