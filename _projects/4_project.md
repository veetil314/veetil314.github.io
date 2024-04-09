---
layout: page
title: Estimating Ground Distances and Heights using Projective Geometry in Monocular Camera Images
description: Estimating ground distances and heights from monocular camera images using projective geometry principles, including homography, vanishing points, and cross-ratio, without explicit camera calibration.

 
img:
importance: 3
category: work
---

# 

## Introduction
Calculating ground distances and heights from monocular camera images can be challenging due to the lack of depth information. However, by leveraging the principles of projective geometry, we can estimate these measurements without the need for explicit camera calibration or statistical methods. This article explores the use of homography, vanishing points, and the cross-ratio to determine ground distances and heights in images, with a focus on applications such as social distancing monitoring.

## Homography and Ground Plane
Homography is a transformation matrix that aids in projecting points from one plane to another. In the context of ground distance estimation, we ideally obtain four reference points on the ground plane with known distances. These points can be used to calibrate ground distances and calculate a desired distance guideline, such as a 6-foot social distancing radius. By transforming pixel coordinates on the image plane to real-world coordinates relative to the reference points, we can verify the distance between any two points in physical space.

## Projective Geometry Invariant Ratios
In cases where reference points with known distances are not available, we can rely on projective geometry invariant ratios to measure distances. This approach allows us to estimate distances without performing camera calibration or employing statistical methods. The key components required for distance estimation are the homography transformation matrix and a scale factor for converting pixel measurements to real-world distances.

## Vanishing Points and Horizon Line
According to the principles of projective geometry, parallel lines in the real world converge to a point called the vanishing point, which is considered to be at infinity. In an image, we can identify vanishing points for different sets of parallel lines, such as V1 and V2 in Figure 1. These vanishing points lie on a line called the horizon line or vanishing line.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vanish2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1. Vanishing points from different groups of parallel lines form the vanishing line
</div>


The horizon line possesses an important property: it is located at the same height as the camera's focal point. This means that the horizon line provides us with the exact height of the camera, without the need for explicit calibration methods.

## Cross-Ratio
The cross-ratio is a numerical invariant of an ordered 4-tuple of points on a line or four points from concurrent lines in a plane. It plays a crucial role in projective geometry because it remains constant under projective transformations. In other words, if we have four points on a line, the ratio between them remains the same, regardless of the point ordering, as illustrated in Figure 2.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vanish1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2. Cross-ratio of four points on a line
</div>


The cross-ratio is particularly useful for height estimation in the image plane. By understanding the cross-ratio and the ability to compute lengths from image measurements using projective geometry properties, we can calculate real heights from vanishing points and lines.

## Height Estimation Procedure
Given the horizon line, the vertical vanishing point, and one reference height, we can compute the height of any point (from the ground plane) by specifying the point and its projection on the ground plane in the image. The procedure, as illustrated in Figure 3, involves the following steps:

1. Draw a line from the base of the reference object to the horizon line, passing through the base of the object to be measured.
2. Draw another line from the intersection of the horizon line and the previous line to the reference object, passing through the top of the object to be measured.
3. The junction of the previous line with the reference object will provide the point that determines the segment d₂.
4. Compute the height using the formula shown in Figure 3, where d₁ and d₂ are distances in pixels.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vanish3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3. Measuring heights using cross ratio 
</div>


## Implementation for Social Distancing
To estimate the ground 6-foot distance for social distancing, we can utilize a combination of properties. First, we identify natural properties of objects in the image to draw four points corresponding to a rectangle on the ground plane, such as using parallel lines like road boundaries.

Next, we draw the vanishing line using various lines on the ground plane. The cross-ratio is employed to verify people's heights as they appear in the image. The height of an object can be calculated using vanishing points Vx, Vy, and Vz. We assume that the Vz vanishing point is not infinite and can be determined using the human head-to-bottom measurement. The Vx and Vy vanishing points are calculated using opposite parallel lines in the homography rectangle in the image plane.

After drawing the horizon line, we locate the intersection point (vertex) of the line passing through the bottom points of the people we want to measure with the horizon line. Then, we draw a line passing through the vertex and the top of a known reference object, intersecting with the line passing through the top and bottom of an unknown object. This determines the intersection point, referred to as the reference object.

Using the cross-ratio method, we can calculate the height, assuming average heights of 5.3 feet for women and 5.8 feet for men. If reference heights are available, such as electric posts or buildings, they can be used, provided they are consistent with the vanishing line derived from the homography reference rectangle. If there is a discrepancy, the reference rectangle is adjusted.

To ensure the accuracy of the height estimation, we can use the homography points as a validation measure. If the homography points are taken incorrectly, the estimated height will deviate from the expected range by more than 10%, prompting an adjustment of the points.

## Conclusion
By leveraging the principles of projective geometry, such as homography, vanishing points, and the cross-ratio, we can estimate ground distances and heights from monocular camera images without the need for explicit camera calibration. This approach has practical applications, such as monitoring social distancing compliance using a 6-foot guideline.

The procedure involves identifying vanishing points, drawing the horizon line, and utilizing the cross-ratio to calculate heights based on reference objects or assumed average heights. While the accuracy of the estimation depends on the correct selection of homography points and consistent vanishing lines, this method provides a valuable tool for extracting meaningful distance and height information from monocular camera images.