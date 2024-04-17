# Concealed object detection using terahertz video

This project focuses on concealed object detection utilizing terahertz video data. Here we used depthwise and depth-wise separable convolutions instead of normal convolutions in YOLOv5 and YOLOv8.

**Dataset**
Our dataset comprises terahertz videos sourced from a publicly available collection by [https://www.fullvision.ru/](https://www.fullvision.ru/). Encompassing 22 distinct classes, the dataset encompasses both dangerous (e.g., knife, pistol, AK) and non-dangerous items (e.g., A4 paper, cigarette box). We have converted this dataset into frames for comprehensive analysis. A glimpse of some dataset classes is displayed below:

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/1db3bbb7-f168-444a-a0ba-78489f940a4a" width="50%">

To further enhance the dataset, we applied data augmentations using [https://app.roboflow.com/](https://app.roboflow.com/). A sample showcasing the augmented data is presented below:

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/5fe5c9f0-a478-4a20-834d-7c92a0b8db04" width="30%">


**YOLOv5m**
The YOLOv5m model excels in real-time concealed object detection. Its architecture includes:
- backbone (CSPDarkNet53 for feature extraction)
- neck (PANet for feature combination)
- head (predicts object details).
The backbone takes in the input tensor, uses CSPDarkNet53 with unique features for robust pattern capture. The neck employs PANet for accurate feature amalgamation, enhancing detection. The head predicts bounding boxes, objectness scores, and class probabilities, ensuring comprehensive detection. This multi-scale approach adapts to various object sizes, making YOLOv5m versatile in concealed object detection scenarios.

**Structure of YOLOv5m**
The architecture of the YOLOv5m model is illustrated below:

![yolov5m_original_arch](https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/4b7d9617-197d-4102-9b9a-6193d7a6cf18)

**YOLOv8m**
Similar to the YOLOv5 architecture, the YOLOv8m architecture also includes:
- backbone (CSPDarkNet53 for feature extraction)
- neck (PANet for feature combination)
- head (predicts object details)
The backbone takes in the input tensor, uses CSPDarkNet53 with unique features for robust pattern capture. The neck employs PANet for accurate feature amalgamation, enhancing detection. The head predicts bounding boxes, objectness scores, and class probabilities, ensuring comprehensive detection. This multi-scale approach adapts to various object sizes, making YOLOv5m versatile in concealed object detection scenarios. The difference between the YOLOv5 and YOLOv8 models are:
- C3 layers in YOLOv5 are replaved by C2F layers in YOLOv8
- The number of blocks of each type are different
  Other than these, both YOLOv5 and YOLOv8 have similar architecture.


**Structure of YOLOv8m**
The architecture of the YOLOv8m model is illustrated below:

![yolov8m_original_arch](https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/26577fe2-ee10-464e-8dac-0ac57374e434)

  

