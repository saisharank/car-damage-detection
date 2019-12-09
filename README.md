# Car-Damage-Detection

This Deep Learning project can be divided into 3 phases: Complete or Partial Damage Detection; Damage Classification

There is no standard dataset for the images. So need to collect the required images from Google like front or rear or left or right side damage into separate folders for both training and testing.

#### Complete or Partial
After getting the images, the model first checks whether full required side of the car is taken or partial is taken. If partial photo is taken, the user has to take the full photo required side of the car. This model is developed using MobileNet, a pre-trained model with an accuracy of 83%.

In order to detect the damage along with the part name, the training images must be labelled. The labels are stored in xml file and converted to a csv and sent for training along with images. LabelImg tool is used for labelling.

  Step 1 : Open terminal
  
  Step 2 : Type sudo apt-get install pyqt5-dev-tools* -y and press Enter.
  
  Step 3 : Type sudo pip install lxml and press Enter
  
  Step 4 : Now clone the labelImg GitHub repository on your machine in required folder by git clone https://github.com/tzutalin/labelImg
  
  Step 5 : Change directory into the labelImg directory cd labelImg
  
  Step 6 : Type make qt5py3
  
  Step 7 : Type python labelImg.py

The labelImg window opens up

Labelling:
  Step 1 : If you wish to select one photo, Click on Open and slect the required pic. Click on Open Dir to select the folder which contain images.
  
Step 2 : Click on Create Rect Box and highlight the required area. A dialog box opens where we need to label it and Click OK.
Perform this step as per required.

Step 3 : Click on Save. Save it with extension .xml

#### Damage Detection
  After getting full image of the part of car, the damage is detected on all sides of the car. If there is damage, the damage would be highlighted with the part like bonet,bumper etc by getting .xml files as input. This model is developed using SSD MobileNet V2, a light weight model for integrating with mobile app.

#### Damage Classification
  After detecting, the damage classification is done such that which side of the car got damaged (i.e.) Left or Right or Front or Rear is found. This model is developed using InceptionV3, a pre-trained model with an accuracy of 82%.
