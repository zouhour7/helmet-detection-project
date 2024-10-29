# helmet-detection-project

This project demonstrates a helmet detection system using computer vision and deep learning, designed to identify motorcyclists wearing or not wearing helmets. The project’s primary goal is to improve road safety through automated monitoring.

# Project Overview

Dataset: The dataset, structured in COCO format, includes annotated images with bounding boxes for helmet detection.

Data Preprocessing and Augmentation:
The project uses Albumentations for data augmentation, applying transformations like resizing, flipping, and color adjustments.
Augmentation helps to make the model more robust, and bounding boxes are converted to fit the input format required by the detection model.

Custom Dataset Class:
A HelmetDetection class loads and processes the dataset.
Images and bounding boxes are extracted, and boxes are formatted for compatibility with the model.

Model Architecture:
A pre-trained Faster R-CNN model with a MobileNetV3-Large backbone is fine-tuned for helmet detection. The model’s classifier head is adjusted to recognize relevant classes.
Training is handled with an SGD optimizer over multiple epochs, tracking loss to improve model performance.

Evaluation and Inference:
Model predictions are evaluated on test images, with bounding boxes drawn around detected objects.
Detections above a confidence threshold are annotated for visualization.

Video Processing with OpenCV:
OpenCV is used to handle video input, extracting frames and applying the trained model to detect helmet use.
Annotated frames are compiled back into a video, showing bounding boxes for detected objects.

# output 

https://github.com/user-attachments/assets/80527ba6-bf6f-4635-8229-3e7913af38f7
