# Anomaly Detection in Images

<center>
  <image src="https://media.giphy.com/media/f73urdknsWliIEZiDw/giphy.gif" width="900" height="600"/><br><br>
</center>

### The Mission

The project is based on the use case by [Faktion](https://www.faktion.com/) and it is to find rare anomalies in dice images through any of the computer vision approaches.

![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_25199_cropped.jpg?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_29052_cropped.jpg?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_29214_cropped.jpg?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_29624_cropped.jpg?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_25064_cropped.jpg?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/17_11_21_anomalies_017.png?raw=true) ![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_25918_cropped.jpg?raw=true)


### The Goal

The goal is to maximize the F1 score.

<center>
  <image src="https://miro.medium.com/max/1400/1*iXh-laAdl3gcddkHpJxnLw.png" width="800" height="200"/><br><br>
</center>

### Dataset

The dataset was provided in two folders. One with train set and another with test set. Both had dice images divided in 11 folders and one with the anomalous ones.
The train set has around 6000 normal images and 300 anomalous ones. The test set had around 300 normal and 52 anomalous images.

### Approach used

I have used the numpy approach to classify the images in the correct classes and find the anomalies. 
For that I tried two methods:
* __Structural Similarity Index (SSIM)__: The Structural Similarity Index (SSIM) is a perceptual metric that quantifies image quality degradation* caused by processing such as data compression or by losses in data transmission. It is a full reference metric that requires two images from the same image capture— a reference image and a processed image.

* __Template matching__ :Template matching is a technique in digital image processing for finding small parts of an image which match a template image. It can be used in manufacturing as a part of quality control, a way to navigate a mobile robot, or as a way to detect edges in images.

### Method

A template is created for every dice face with which the source image is to be matched.
A threshold needs to be set for the index. If the index for an image is above the threshold, it is considered normal and if not then it is anomalous.

### Visuals

![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_2.png?raw=true) 
![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_1.png?raw=true) 
![](https://github.com/N1chelle/Anomaly-Detection-in-Images/blob/main/Images/img_3.png?raw=true)

### F-1 score

* Train set = 0.78
* Test set = 0.72

### Challenges

* Some images are wrongly matched with a different template.
* Some normal images are classified as anomalous and vice versa.
* It works well for certain dice faces but not that well for others.

### Improvements

I would like to improve the code by:
* Adding more varied templates.
* Preprocessing the templates as well as the source images.
* Experimenting with different threshold values to see what gives the best F1 score.
* Trying other approaches like machine learning, transfer learning and deep learning algorithms.

### Timeline

* Duration: 2 weeks
* Deadline: 10/02/2022 16.30
