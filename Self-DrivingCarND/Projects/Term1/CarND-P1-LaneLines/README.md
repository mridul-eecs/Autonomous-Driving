# Finding Lane Lines on the Road
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

[Project Repository](https://github.com/udacity/CarND-LaneLines-P1)

[Project Rubric](https://review.udacity.com/#!/rubrics/1967/view) 

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.

First, I converted the images to grayscale, then I use guassian blur to make the greyscale images smooth. Secondly, I choose the mask region to reduce the Lane detection region.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by average and extrapolate the slope. In the *draw_lines* function, I use some tricks to reduce the noise signal, as following

1. define the range of slope,
2. define the range of lanes


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be the end point of lane was easy to be effected by noise.

Another shortcoming could be unstable when environment changes.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use a smarter classifier like SVM to detect lanes.

Another potential improvement could be to choose a good model to represent lanes

![alt text][image1]
