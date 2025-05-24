# Brain Tumor Detection using YOLO

This repository contains code and resources for detecting brain tumors using the YOLO (You Only Look Once) object detection model. The project leverages the ultralytics YOLO library to train and evaluate a custom model on a brain tumor dataset.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Training](#training)
- [Inference](#inference)
- [Results Visualization](#results-visualization)
- [Requirements](#requirements)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)


## Installation


1. Install the required Python libraries:
    ```bash
    pip install -r requirements.txt
    ```



## Training
To train the YOLO model, ensure you have configured a YAML file with paths to your training and validation data. Example command to train:

```python
from ultralytics import YOLO
model = YOLO('yolov8n.pt')
model.train(data='data.yaml', epochs=50, imgsz=640)
```

## Inference
To run inference on an image:
```python
from ultralytics import YOLO

trained_model = YOLO('path/to/best.pt')
results = trained_model('path/to/image.png')
```

## Results Visualization
Use Matplotlib to visualize results:
```python
import matplotlib.pyplot as plt

image_array = results[0].plot()
plt.imshow(image_array)
plt.axis('off')
plt.show()
```

## Requirements
- Python 3.8 or higher
- Libraries: ultralytics, matplotlib, pillow

Install all dependencies using:
```bash
pip install -r requirements.txt
```

## Usage
1. Train the YOLO model using your dataset.
2. Perform inference on new images to detect brain tumors.
3. Visualize and analyze the results.



Feel free to contribute to this project by submitting issues or pull requests!"
}

