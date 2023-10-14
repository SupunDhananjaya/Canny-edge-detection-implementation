# Canny-edge-detection-implementation

Canny edge detection is a popular image processing technique used to identify edges in images. It was developed by John F. Canny in 1986. The process involves several steps:

Noise Reduction: The first step is to apply a Gaussian blur to the image. This helps in reducing noise and fine details, which can interfere with edge detection.
Gradient Calculation: Next, the gradients (rate of change) of intensity in the image are calculated. This is typically done using techniques like Sobel or Prewitt operators. These operators highlight areas of rapid intensity change, which often correspond to edges.
Non-maximum Suppression: After gradient calculation, the algorithm performs non-maximum suppression. This involves thinning down the detected edges to a one-pixel wide line. It does this by considering the gradients and keeping only the local maxima.
Double Thresholding: The edges are then classified into strong, weak, and non-relevant based on their gradient strengths. Pixels with gradients above a high threshold are considered strong edges, while those below a low threshold are considered non-edges. Pixels with gradients in between are labeled as weak edges.
Edge Tracking by Hysteresis: This step aims to extend the strong edges while suppressing weak ones that are unlikely to be actual edges. It does this by following the connected path of strong edges. If a weak edge is connected to a strong edge, it is considered part of the edge. Otherwise, it is suppressed.

The result is a binary image where strong edges are well-defined, and weak edges have been either eliminated or connected to strong ones. Canny edge detection is widely used in computer vision applications such as object detection, image segmentation, and feature extraction.

This repository includes a sample Canny edge detection implementation.
