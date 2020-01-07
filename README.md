# Bad Print Detector

## Requirements for ML(Machine Learning) part



### 0. Spaghetti monster

 Spaghetti monster usually happens mid-print or when the printing is nearly done. The printer still continues to print; thus wasting filament, electricity and time. At leFab 3D, they use hobbyist 3d printers with Octoprint installed. They have many failed prints that fail and continue to waste more resources after failing.

<img src="./img/spaghetti.jpg" alt="spaghetti" style="zoom:33%;" />



### 1. Objective of ML part

 In the first phase, we will integrate the open source TheSpaghettiDetective plugin into Octoprint and replace the object detection algorithm it uses (YOLO v2) with (YOLO v3). So our ML part needs to  implement a deep learning model for object detection. And this model must detect the spaghetti monster.

 In the second  phase, we will create our own Octoprint plugin that does object detection directly on the Raspberry Pi.  We need a seperate server for detection because Raspberry Pi is not enough performance to detect objects using our model. We have no additional hardware resources, so we use a separate server through GCP. Thus our ML part must implement the model to run on GCP environment.



### 2. Task requirements

Primary:

​	1)  Create a dataset of 500 bad print images.

​	2)  Label images with bounding boxes.

​	3)  Train object detector (SSD), (RetinaNet), (YOLO v3) using PyTorch or fastai.

Secondary:

​	1)  Make survey on our spaghetti detection models.  

​	2)  Add function to detect other errors. (e.g. warping, first layer issue ...) 



### 3. Technical requirements

Machine Learning:

 - fastai
 - PyTorch

Text editor:

 - jupyter notebook
 - vs code

Other computing skills:

- Google Cloud Platform

- Git, GitHub

  

### 4. Resources

- Spaghetti momnster image: https://www.prusa3d.com/spaghetti-monster/
- The Spaghetti Detective: https://www.thespaghettidetective.com/ 