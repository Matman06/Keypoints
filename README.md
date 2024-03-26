# Image Matching Using Keypoints Method

## Overview

This repository contains an implementation of an image matching method that utilizes keypoints to identify and track the same object across multiple images. The method is based on detecting keypoints in images, extracting their descriptors, and then matching these descriptors between pairs of images. This approach has been developed and tested using images from Vincent Lepetit's website, providing a practical context for the implementation and evaluation of the algorithm.

## Methodology

The implemented method involves several key steps:
1. **Keypoint Detection**: Detects points of interest in each image using the Harris corner detection algorithm. This step is crucial for identifying features in the images that are distinctive and trackable across different views.
2. **Descriptor Extraction**: Extracts descriptors around each detected keypoint. These descriptors encapsulate the local appearance of the image around the keypoint, enabling the comparison of keypoints across images.
3. **Keypoint Matching**: Matches keypoints between images by comparing their descriptors. The matching process identifies pairs of keypoints in two images that are likely to correspond to the same point in the physical scene.
4. **Estimation of Object Position**: Utilizes the matches to estimate the position and scale of an object of interest (e.g., a painting) across multiple images. This step adapts to changes in object size and occlusions.

## Implementation Details

The implementation is done in Python, utilizing libraries such as OpenCV for image processing and NumPy for numerical computations. The repository includes functions for each step of the method, along with examples demonstrating the application of the method to a series of images.

## Results

The method has been tested on a series of images featuring reproductions of paintings, with promising results. The algorithm successfully tracks the position of the object across images, despite variations in scale, orientation, and partial occlusions. Notably, image number 5 presented a challenge due to a significant occlusion; however, the methodology showed resilience by accurately identifying the object in the majority of the images.

## Future Work

To further enhance the model's adaptability to changes in object size, future work could include the development of a dynamic scaling mechanism. This would allow the estimated rectangle, representing the object's position, to adjust its size more accurately according to each image, providing a more comprehensive and robust solution for image matching challenges.

## Acknowledgments

This project was inspired by the work and resources provided by Vincent Lepetit. The images used for testing and development of the algorithm were sourced from his website, serving as a valuable dataset for implementing and evaluating the image matching method.
