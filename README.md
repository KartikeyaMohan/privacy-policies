FAST Feature Detector in Python

This code uses the OpenCV library to perform the FAST (Features from Accelerated Segment Test) feature detector on two grayscale images and visualizes the detected points.

Requirements
    OpenCV (cv2)
    Numpy

Usage
If you wish to use it for images other than the ones used, replace the filenames 'S1-im1.png' and 'S1-im2.png' with the filenames of the images you want to process.
Run the code using your preferred Python environment.
The code will detect the keypoints in both images using the FAST feature detector and draw them on the original images. The resulting images with keypoints will then be saved to files named S1-fast.png and S2-fast.png, respectively.

Results
The output images will show the keypoints detected by the FAST feature detector, represented as red circles. The number and distribution of the keypoints will vary depending on the content of the input images.


FASTR Feature Detection

This repository contains code to perform FAST feature detection with Harris cornerness measure and save the visualizations of the detected points. The code computes the Harris cornerness measure for each detected FAST feature and eliminates weak FAST points by defining a threshold for the Harris metric. The threshold is fixed for every image used. The resulting features are referred to as FASTR points.

Requirements
    Python 3.x
    OpenCV 4.x
    Numpy

Usage
To run the code, simply execute the fast_harris.py file in a Python environment that has the required packages installed. The code requires 2 images as input, and will save the visualizations of the detected FASTR points for each image as S1-fastR.png and S2-fastR.png.

Explanation
The code uses the OpenCV library to perform FAST feature detection and the Harris cornerness measure. The FAST algorithm is used to detect corner points in the images, while the Harris cornerness measure is used to eliminate weak FAST points by defining a threshold. The resulting FASTR points are then visualized and saved as images.

The average computation time of FAST and FASTR features is computed by taking the average of the processing time for all the images used. The difference in computation time between FAST and FASTR features depends on the number of images processed and the complexity of the Harris cornerness measure calculation.

By comparing the FAST and FASTR visualizations, we can see which points were discarded after the threshold was applied. The FAST visualization shows all the features detected by the FAST algorithm, while the FASTR visualization shows only the features that passed the Harris cornerness threshold. The comparison of the FAST and FASTR visualizations allows us to see which points were discarded as a result of the Harris cornerness threshold, and helps us understand the impact of the threshold value on the feature detection results.


FAST Point Matching ReadMe

This ReadMe file provides information about the code for implementing FAST (Features from Accelerated Segment Test) point matching in python using OpenCV library. The code performs feature detection and matching between two images.

Prerequisites
Before running the code, make sure you have the following installed:

    Python 3.x
    OpenCV library for Python
    Numpy library for Python

Running the code
To run the code, follow these steps:

Open a terminal or command prompt
Navigate to the directory where the code is stored
Run the code using the command python PointDes_Matching_FASTR.py
Enter the name of the first image in the source code
Enter the name of the second image in the course code before running. 
The code will perform feature detection using the FAST algorithm and match the features between the two images
The matched points will be visualized and saved as an image in the same directory with the file name S1-fastMatch.png (or according to how you want it) 

Understanding the code
The code performs the following steps to perform FAST point matching:

Read the two images
Convert the images to grayscale
Detect keypoints using the FAST algorithm
Compute the FAST descriptor for the keypoints
Match the features between the two images using the BFMatcher class in OpenCV
Visualize the matched points using the drawMatches function in OpenCV
Save the visualization of the matched points as an image

Note
The code assumes that the images are in the same directory as the code. If the images are stored in a different directory, make sure to specify the complete path to the images in the code.

ReadMe for FASTR Point Matching

This ReadMe file provides information on how to use the code for matching FASTR points between two images using OpenCV in Python.

Requirements
    Python 3.x
    OpenCV library (version 4.5.3 or higher)

Overview
This code uses the OpenCV library to detect and describe keypoints in two images using the FASTR algorithm. The keypoints are then matched between the two images, and the resulting matches are visualized and saved as an image.

Usage
Clone or download the code to your local machine.
Place the two images you want to match in the same directory as the code.
Open the code in your preferred Python environment or IDE.
Update the file names of the two images in the code to match the names of the images you want to use.
Run the code.
The resulting image of the matched FASTR points will be saved as "S1-fastRMatch.png" in the same directory as the code.
Change the name in the code to make it work for the other files as well. 

Additional Information
The code uses the BFMatcher function from the OpenCV library to perform the keypoint matching.
The threshold for matching keypoints can be adjusted by updating the distance_threshold variable in the code.
The visualization of the matched keypoints is done using the drawMatches function from the OpenCV library.
Conclusion
This code provides a basic implementation of the FASTR keypoint matching algorithm using the OpenCV library in Python. It can be used as a starting point for more complex computer vision projects.


ReadMe for Panorama RANSAC
Prerequisites
    Python
    OpenCV installed
    numpy


Running the code

Clone or download the code repository.
Make sure you have placed the two pictures that you want to stitch in the same directory as the code file.
In the code file, update the filenames for the two pictures with the names of the two pictures you want to stitch.
Open a terminal or command prompt and navigate to the directory where the code file is located.
Run the code by executing the following command:
Copy code
python Panorama_for2.py
Output
The code will generate a new picture that is the result of stitching the two pictures together. The stitched picture will be saved in the same directory as the code file with the name stitched_image.png.


