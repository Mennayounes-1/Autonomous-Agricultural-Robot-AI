#  Autonomous Agricultural Robot – AI & Computer Vision

An AI-powered autonomous agricultural robot designed to detect plant leaves and identify plant diseases using Computer Vision and Deep Learning.

## Project Overview

This project was developed as a Graduation Project.

The main goal is to build an intelligent agricultural robot capable of analyzing plants in real-world environments and detecting plant diseases automatically.

The AI system uses a two-stage computer vision pipeline:

1. **YOLOv8-OBB** for plant leaf detection and localization.
2. **Custom CNN** for plant disease classification.

## AI Pipeline

Camera Image  
↓  
YOLOv8-OBB – Leaf Detection  
↓  
Detected Leaf  
↓  
Custom CNN – Disease Classification  
↓  
Disease Prediction

##  Stage 1 – Leaf Detection

YOLOv8-OBB is used to detect and localize plant leaves.

The detection model was trained to recognize 7 classes representing different plant health and disease severity categories.

The model achieved:

- Precision: **93.6%**
- Recall: **84.4%**
- mAP@50: **99.0%**
- mAP@50-95: **92.1%**

##  Stage 2 – Disease Classification

After detecting the plant leaf, the detected region is passed to a Custom Convolutional Neural Network (CNN).

The classifier was trained on **38 plant disease and healthy classes**.

Performance:

- Validation Accuracy: **99.08%**
- Input Image Size: **224 × 224**
- Framework: **TensorFlow / Keras**

Several deep learning architectures were also explored and compared, including:

- Custom CNN
- MobileNetV2
- EfficientNetB0
- ResNet50
- VGG16

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- YOLOv8
- Ultralytics
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib
- Computer Vision
- Deep Learning

##  Repository Contents

- `YOLOv8_OBB_Plant_Disease_Final (1).ipynb` – YOLOv8-OBB training, evaluation and two-stage inference pipeline.
- `Model Structure.ipynb` – Plant disease classification model development and comparison.
- `Imgae_Test.ipynb` – Image testing and prediction.
- `CustomCNN_history.png` – Custom CNN training history.
- `CustomCNN_validation_confusion_matrix.png` – Validation confusion matrix.
- `CustomCNN_test_confusion_matrix.png` – Test confusion matrix.
- Classification reports – Detailed evaluation results.

##  Project Goal

The goal of this project is to combine Artificial Intelligence, Computer Vision and Robotics to support precision agriculture by automatically detecting unhealthy plants and identifying plant diseases.

##  My Contribution

My main contribution to the graduation project focused on the Artificial Intelligence and Computer Vision system, including:

- Preparing and processing plant image datasets.
- Training and evaluating deep learning models.
- Developing the YOLOv8-based leaf detection system.
- Developing and evaluating the Custom CNN disease classifier.
- Integrating detection and classification into a two-stage AI pipeline.
- Testing the system on plant images and analyzing model performance.

##  Future Improvements

Future improvements may include:

- Real-time deployment on the agricultural robot.
- Optimization for edge devices such as Raspberry Pi.
- Expanding the dataset with more real-world field images.
- Improving disease detection under different lighting and environmental conditions.
