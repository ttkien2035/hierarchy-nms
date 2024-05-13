# hierarchy-nms
This tool provides a Python implementation of the Modified Non-Maximum Suppression algorithm to handle object detection scenarios where class hierarchies are important.

## Features
- Confidence Thresholding: Filters out bounding boxes with confidence scores below a user-defined threshold.
- Class-wise Suppression: Within the same class, suppresses less confident bounding boxes that overlap more than a specified Intersection over Union (IoU) threshold.
- Hierarchical Suppression: For overlapping boxes of different classes, if one is the parent of the other, the parent is suppressed, which is crucial for maintaining semantic accuracy in hierarchical object detection.
## Requirements
Python 3.6 or higher
NumPy library
## Installation
Clone the Repository: To get started, clone this repository using:

```
git clone https://github.com/ttkien2035/hierarchy-nms.git
```

## Structure
modified_nms.py: The main Python script containing the modified NMS algorithm.
## Usage
To use the Modified NMS in your project, follow these steps:

- Prepare Your Data: Ensure you have bounding boxes, their associated confidence scores, class labels, and the class hierarchy ready.

- Edit the Script (if needed): Modify the example in the if __name__ == "__main__": block of modified_nms.py to use your data.

- Run the Script: Execute the script from the command line:
```
python modified_nms.py
```