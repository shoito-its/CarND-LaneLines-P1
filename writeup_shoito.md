# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I define the cannt parameter,and create canny edge image.

Third , The image was cut out only in the part necessary for detection.

Forth , I define the Hough transform parameters , and Detected lines using Hough transform. 

Finally, I created weighted image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function.

I calclation bias and average detect coordinate , then calclation new coordinate.

I already know region of interest, so draw line fron ybottom to region of interest points. 


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen When the car curves.

I only draw straight line , so I can't draw curve lines.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use another fitting algorithm which can also deal with curve fitting (second-order polynomial) such as Robust nonlinear regression.
