# Caffe-Data-Augmentation

The original repository for Caffe, developed by the Berkeley Vision and Learning Center  and community contributors, is at  ([BVLC](http://bvlc.eecs.berkeley.edu)).

This project adds a data augmentation feature to caffe, augmenting the data in 9 several ways. 

The ways in which the data is augmentated is explained here:
1. Image Translation - a random shift in a x and y axis pixels of the entire image. The shift has uniform probability between -7 and 7.
2. Image Rescailing - shrinking or enalrgin the image (before cropping) by a random unifrom factor between 0.8 and 1.2.
3. Horizontal Flipping - flipping the image in the horizontal axis.
4. Vertical Flipping - flipping the image in the vertical axis.
5. Elastic Deformation with Random Interpolation - dislocate pixels and use OpenCV interpolations method randomly.
6. Color Noising - adding a small independent noise to each color channel of the image.
7. Brightness Noising - adding a small noise to the brightness of each pixel.
8. Small Blurring - convolving the image with small random-sized blurring kernel.
8. Single Random Transformation - choosing a transformation at random.
9. Multiple Random Transformations - chooses each transofrmation with probability 1/7, such that the mean is one transformation for every image. 

The desired transformation(s) is chosen by parameter transform_type within the prototxt file for the data layer. The value of the parameter corresponds to the transform schemes described above.
For example, '''transform_type=4''' uses vertical flipping as it's transformation.


This project was developed by Shani Rehana, Baruch Epstein and Shahar Katz.
