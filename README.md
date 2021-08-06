# Age-and-Gender-Detection
To build a gender and age detector that can approximately guess the gender and age of the person (face) in a picture or through webcam.

In this Python Project, I had used Deep Learning to accurately identify the gender and age of a person from a single image of a face. I used the models trained by Tal Hassner and Gil Levi. The predicted gender may be one of ‘Male’ and ‘Female’, and the predicted age may be one of the following ranges- (0 – 2), (4 – 6), (8 – 12), (15 – 20), (25 – 32), (38 – 43), (48 – 53), (60 – 100) (8 nodes in the final softmax layer). It is very difficult to accurately guess an exact age from a single image because of factors like makeup, lighting, obstructions, and facial expressions. And so, I made this a classification problem instead of making it one of regression.

Additional Python Libraries Required :

OpenCV
pip install opencv-python

argparse
pip install argparse
   
 The contents of this Project :

opencv_face_detector.pbtxt

opencv_face_detector_uint8.pb

age_deploy.prototxt

age_net.caffemodel

gender_deploy.prototxt

gender_net.caffemodel

a few pictures to try the project on
detect.py

For face detection, we have a .pb file- this is a protobuf file (protocol buffer); it holds the graph definition and the trained weights of the model. We can use this to run the trained model. And while a .pb file holds the protobuf in binary format, one with the .pbtxt extension holds it in text format. These are TensorFlow files. For age and gender, the .prototxt files describe the network configuration and the .caffemodel file defines the internal states of the parameters of the layers.

Usage :

Download my Repository

Open your Command Prompt or Terminal and change directory to the folder where all the files are present.

Detecting Gender and Age of face in Image Use Command :
  
  python detect.py --image <image_name>

Note: The Image should be present in same folder where all the files are present

Detecting Gender and Age of face through webcam Use Command :
  
  python detect.py
  
 Working: 
 
python detect.py --image girl1![Screenshot (200)](https://user-images.githubusercontent.com/55014144/128483400-f3ba86f1-014c-441f-a509-a34a688aed4e.png)
.jpg





Gender: Female

Age: 22-25 years


>python detect.py --image man2.jpg![Screenshot (163)](https://user-images.githubusercontent.com/55014144/128494713-261ee2c4-b11d-4ab0-b26e-385ffc4c1099.png)


Gender: Male


Age: 25-32 years









