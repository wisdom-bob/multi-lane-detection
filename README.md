**Finding Lane Lines on the Road** 

Overview
---
According to udacity projects of CarND-LaneLines-P1-master and CarND-Advanced-Lane-Lines-master, design an improved algorithm to obtain real-time multi-lane line detection algorithm. 
as an integral part of lab project-- Automotive Vision ADAS.

pipeline thinking
---
Grayscale, Gauss filtering, image binarization block by block with Canny operator (the purpose of segmentation is to improve detection accuracy, reduce processing area, more concentrated features, better processing results) and then extract edges based on regions of interest; on this basis, Hough transform (setting the shortest line segment and line segment) is carried out. Interval, angle, etc.) Lane features are obtained. Oblique straight lines are obtained through feature processing. Similarity matching and classification are carried out. Lane lines without vanishing points are eliminated based on vanishing point characteristics. Lane lines are smoothed based on smoother tracker to get the final lane.


