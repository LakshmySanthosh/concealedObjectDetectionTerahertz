# Concealed object detection using terahertz video

In this project, from a publically available terahertz video dataset, using the YOLOv5m, a model is created to detect concealed objects. Hyperparameter tuning helps in getting better accuracy in object detection. To tackle the problem of overfitting, we use data augmentations on the dataset.


**Dataset**
The dataset consists of terahertz videos obtained from a publically available terahertz dataset by [https://www.fullvision.ru/](https://www.fullvision.ru/). It consists of 22 classes of images comprising of dangerous(knife, pistol, AK, etc) and non-dangerous(A4paper, cigarettebox, etc). We are using this dataset by converting it into frames. Some of the classes of the dataset are shown below.
<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/1db3bbb7-f168-444a-a0ba-78489f940a4a" width="50%">

We did some data augmentations on the dataset using [https://app.roboflow.com/](https://app.roboflow.com/), a sample of the augmented data is shown below
<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/5fe5c9f0-a478-4a20-834d-7c92a0b8db04" width="30%">


**YOLOv5m**
The YOLOv5m model excels in real-time concealed object detection. Its architecture includes:
- stem (initiates processing)
- backbone (CSPDarkNet53 for feature extraction)
- neck (PANet for feature combination)
- head (predicts object details).
The stem preprocesses input images, and the backbone uses CSPDarkNet53 with unique features for robust pattern capture. The neck employs PANet for accurate feature amalgamation, enhancing detection. The head predicts bounding boxes, objectness scores, and class probabilities, ensuring comprehensive detection. This multi-scale approach adapts to various object sizes, making YOLOv5m versatile in concealed object detection scenarios.

**Structure of YOLOv5m**

<img src="https://github.com/LakshmySanthosh/concealedObjectDetectionTerahertz/assets/121610033/265a81d0-e913-4b1a-a721-60fdab2f920c" width="50%">




