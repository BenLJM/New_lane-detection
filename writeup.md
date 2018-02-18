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

My pipeline is basically follow the same process as the example in previous quiz. It is consisted of 8 steps. First, I read in the image and print out the info to assist myself. Then, I converted the image to grayscale and blur the image using Gaussian Blur method to get rid of detail that I don’t need. I used Cany Edge detection method to find the lanes after that. Creating an area of interest is my next step which help the program focus on the area that lane lines most likely show up. Finally, I draw lines using hough_lines function and combine the result with initial image to give the final image. 


### 2. Identify potential shortcomings with your current pipeline

I was stuck when I notice that my pipeline cannot draw complete lines from the bottom. Therefore, I read through Mr. Shibuya’s program and improve it. The draw_Perfect_lines function solve the previous issue but it still cannot distinguish the real lanes and the dark side of road which appear in the challenge problem.

### 3. Suggest possible improvements to your pipeline

A possible improvement will be making my pipeline more precise by converting image to different color space. This will help the program to determine which are the real lanes when the situation in the challenge problem happens.
