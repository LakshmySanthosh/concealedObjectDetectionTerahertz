# Concealed object detection using terahertz video

This project focuses on concealed object detection utilizing terahertz video data. Employing the YOLOv5m model, we have crafted a sophisticated system to identify concealed objects. Rigorous hyperparameter tuning enhances the model's accuracy in object detection, while strategically applied data augmentations mitigate the risk of overfitting.


**Dataset**
Our dataset comprises terahertz videos sourced from a publicly available collection by [https://www.fullvision.ru/](https://www.fullvision.ru/). Encompassing 22 distinct classes, the dataset encompasses both dangerous (e.g., knife, pistol, AK) and non-dangerous items (e.g., A4 paper, cigarette box). We have converted this dataset into frames for comprehensive analysis. A glimpse of some dataset classes is displayed below:

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/1db3bbb7-f168-444a-a0ba-78489f940a4a" width="50%">

To further enhance the dataset, we applied data augmentations using [https://app.roboflow.com/](https://app.roboflow.com/). A sample showcasing the augmented data is presented below:

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/5fe5c9f0-a478-4a20-834d-7c92a0b8db04" width="30%">


**YOLOv5m**
The YOLOv5m model excels in real-time concealed object detection. Its architecture includes:
- stem (initiates processing)
- backbone (CSPDarkNet53 for feature extraction)
- neck (PANet for feature combination)
- head (predicts object details).
The stem preprocesses input images, and the backbone uses CSPDarkNet53 with unique features for robust pattern capture. The neck employs PANet for accurate feature amalgamation, enhancing detection. The head predicts bounding boxes, objectness scores, and class probabilities, ensuring comprehensive detection. This multi-scale approach adapts to various object sizes, making YOLOv5m versatile in concealed object detection scenarios.

**Structure of YOLOv5m**
The architecture of the YOLOv5m model is illustrated below:

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/265a81d0-e913-4b1a-a721-60fdab2f920c" width="50%">
