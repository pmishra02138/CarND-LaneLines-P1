# **Finding Lane Lines on the Road**

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Extrapolate lane lines to draw solid connected lane lines

---

### Reflection

## 1. Pipeline to extract lanes.

#### My pipeline consisted of following main steps:

* Extract edges using canny edge detector
* Connect edges using Hough transform to generate lane lines
* Combine original image and lane lines to highlights lanes

#### Pipeline to generate extrapolated solid connected lane lines:

* Calculate slopes of every line generated after Hough transform
* Separate left and right lines based on positive or negative slopes
* Calculate average point for the left and right lanes
* Based on the slopes and average point calculate connected left and right lanes.
* Combine original image and lane lines

### 2. Identify potential shortcomings with your current pipeline


The main shortcoming of my pipeline is that the results depend the type of edge detector. Further the result of edge detector depends on dine tuning the parameters.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to try and evaluate different edge detectors.
