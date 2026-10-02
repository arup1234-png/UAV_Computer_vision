# UAV Computer Vision for Object Detection

## Overview

This project explores **object detection in UAV/aerial imagery using YOLO and the VisDrone-2019-DET dataset**.

The objective is to develop and evaluate a deep-learning-based computer vision pipeline capable of detecting multiple object categories in challenging aerial scenes, including variations in object scale, viewpoint, background complexity, and image density.

## Project Objectives

* Build an object-detection pipeline for UAV imagery.
* Train a YOLO-based object detection model using the VisDrone dataset.
* Evaluate model performance using standard object-detection metrics.
* Analyze model behaviour on challenging aerial scenes.
* Visualize prediction results and identify areas for improvement.

## Dataset

The project uses the **VisDrone-2019-DET** dataset.

The dataset contains aerial images captured by drones and includes multiple object categories such as:

* Pedestrians
* People
* Bicycles
* Cars
* Vans
* Trucks
* Tricycles
* Awning-tricycles
* Buses
* Motorcycles

For this project, the dataset was organized into training and validation subsets according to the VisDrone detection format.

## Technologies Used

* Python
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## Model Training

The YOLO model was trained using the following configuration:

| Parameter         |                      Value |
| ----------------- | -------------------------: |
| Dataset           |          VisDrone-2019-DET |
| Training Images   |                      6,471 |
| Validation Images |                        548 |
| Image Size        |                  512 × 512 |
| Epochs            |                         20 |
| Batch Size        |                          2 |
| Hardware          |                 NVIDIA GPU |
| Framework         | PyTorch / Ultralytics YOLO |

## Model Performance

The final training results after 20 epochs were:

| Metric    | Result |
| --------- | -----: |
| Precision | 0.3089 |
| Recall    | 0.2334 |
| mAP@50    | 0.1903 |
| mAP@50-95 | 0.1032 |

These results provide a baseline for UAV-based object detection and indicate opportunities for further optimization.

## Challenges

UAV imagery introduces several computer-vision challenges:

* Small object sizes
* Large variation in object scale
* Dense object distributions
* Complex backgrounds
* Different camera viewpoints
* Occlusion between objects
* Limited computational resources during training

## Future Improvements

Potential improvements include:

* Increasing the number of training epochs.
* Experimenting with different YOLO architectures and model sizes.
* Hyperparameter optimization.
* Increasing image resolution.
* Applying appropriate data augmentation.
* Addressing class imbalance.
* Performing error analysis on small-object detections.
* Comparing different object-detection architectures.
* Evaluating inference speed for real-time UAV applications.

## Project Workflow

```text
VisDrone Dataset
       ↓
Data Preparation
       ↓
Dataset Configuration
       ↓
YOLO Model Training
       ↓
Validation
       ↓
Performance Evaluation
       ↓
Prediction Visualization
       ↓
Error Analysis
```

## Results

Example model predictions and training results are available in the `results/` directory.

## Repository Structure

```text
UAV-Computer-Vision-YOLO/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
├── src/
├── configs/
├── results/
└── docs/
```

## Key Takeaway

This project provided practical experience in developing a deep-learning-based object detection pipeline for UAV imagery, including dataset preparation, model training, validation, performance evaluation, and visualization.

The current model serves as a baseline for further experimentation toward more robust aerial object detection.

## Author

**Arupananda Nayak**

M.Sc. Data Science
Computer Vision | Machine Learning | Scientific Computing | Aerospace Analytics
