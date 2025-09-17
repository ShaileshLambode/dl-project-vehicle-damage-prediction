# Vehicle Damage Prediction 🚗💥

Transforming Vehicle Damage Assessment with AI Precision

---

![App Screenshot](app_screenshot.jpg)

*A drag-and-drop interface to detect vehicle damage using AI. Upload a car image (third‐quarter front or rear view), and get a prediction of the damage type.*

---

## Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Model Details](#model-details)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
5. [Usage](#usage)  
6. [Evaluation & Results](#evaluation--results)  
7. [Future Work](#future-work)  
8. [Folder Structure](#folder-structure)  
9. [Contributing](#contributing)  
10. [License](#license)  

---

## Overview

*Vehicle Damage Prediction* is an AI‑powered web application designed to streamline damage assessment of vehicles via images. It supports rapid, automated classification of car damage types from images taken from either a **third‑quarter front** or **rear view**, helping with insurance claims, repair estimates, or inspections.

---

## Features

- **Image Classification**: Detects six kinds of damage/state classes:  
   1. Front Normal  
   2. Front Crushed  
   3. Front Breakage  
   4. Rear Normal  
   5. Rear Crushed  
   6. Rear Breakage  

- **User‑Friendly Interface**: Drag & drop image upload for easy use.

- **Fast Inference**: Once loaded, model gives quick predictions.

- **Focused Use Case**: Optimized for third‑quarter front & rear views of cars.

---

## Model Details

- Base architecture: **ResNet50** (transfer learning).  
- Dataset: ~1,700 images across the 6 classes.  
- Validation accuracy: **≈ 80%** on held‑out validation set.  

Other model details:

- Loss function used (e.g. Cross‑Entropy)  
- Training strategy (data augmentation, epochs, optimizer, learning rate)  
- Any regularization (dropout, weight decay)

---

## Getting Started

### Prerequisites

- Python 3.7+  
- `pip` / venv (or other virtual environment tool)  
- GPU (optional, but helpful for faster training)  

### Installation

```bash
# Clone the repo
git clone https://github.com/ShaileshLambode/dl-project-vehicle-damage-prediction.git

cd dl-project-vehicle-damage-prediction

# Set up virtual environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## Usage

1. Ensure that `model` directory contains the trained model file (if not, train following instructions below or load from checkpoint).  
2. Run the web application:

    ```bash
    python app.py
    ```

3. In your browser, go to `http://localhost:5000` (or the port the app uses).  
4. Upload / drag & drop your car image (third‑quarter front or rear view).  
5. View the prediction.  

---

## Evaluation & Results

| Metric            | Value       |
|--------------------|--------------|
| Validation Accuracy | ~ 80%        |
| Number of Classes   | 6            |
| Number of Images    | ~ 1,700      |

- Confusion matrix analysis  
- Examples of misclassifications  
- Possible biases (e.g. lighting, angle, quality of image)  

---

## Future Work

- Expand dataset: more images (angles, lighting, damage types)  
- Add more classes (e.g. side damage, minor scratches)  
- Improve image preprocessing & augmentation (to handle more real‑world variation)  
- Explore other architectures (e.g. EfficientNet, DenseNet)  
- Deploy model as API / container (Docker)  
- Add more metrics & monitor model drift  

---

## Folder Structure

```
dl-project-vehicle-damage-prediction/
├── app.py
├── model_helper.py
├── model/
│   └── [trained model file(s)]
├── requirements.txt
├── app_screenshot.jpg
├── temp_file.jpg
├── README.md
└── LICENSE
```

- `app.py`: main web app to upload images & get predictions  
- `model_helper.py`: functions to load the model, preprocess image, run prediction  
- `model/`: stores the trained model files  
- `requirements.txt`: all Python dependencies  
- `app_screenshot.jpg`: screenshot for UI reference  

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository  
2. Create your feature branch (`git checkout -b feature/my-feature`)  
3. Make your changes & add tests if applicable  
4. Commit your changes (`git commit -m "Add some feature"`)  
5. Push to branch (`git push origin feature/my-feature`)  
6. Open a Pull Request  

Please follow the code style & add clear documentation for new features.

---

## License

This project is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.

---
