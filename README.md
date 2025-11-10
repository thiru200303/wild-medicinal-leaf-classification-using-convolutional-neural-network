# Wild Medicinal Leaf Classification Using CNN (MobileNetV2)

A deep learning-based system for classifying **21 wild medicinal leaf species** using **Convolutional Neural Networks (CNN)** with **MobileNetV2 Transfer Learning**.

This project aims to support AI-driven botanical research and medicinal plant identification — focusing on flora native to Tamil Nadu, India.

---

## Key Features

- Custom dataset with **3000+ real leaf images**
- **Data Augmentation** to overcome class imbalance
- **MobileNetV2** fine-tuned for classification
- Achieved **94% accuracy**
- Confusion matrix + performance evaluation included
- Maps predictions to **medicinal uses** (knowledge integration)
- Modular and scalable training pipeline

---

## Dataset Details

| Item | Value |
|------|------|
| Total images | 3,000+ |
| Classes | 21 medicinal plant species |
| Collected from | Tamil Nadu, India |
| Format | JPG / PNG |
| Storage size | ~30.5 GB |

🚫 Dataset cannot be fully uploaded to GitHub due to size  
✅ Sample images included  
✅ Class names and metadata maintained

---

## Model Architecture

- Pretrained **MobileNetV2** base
- Global Average Pooling Layer
- Dense Layer (512 neurons)
- Dropout for regularization
- Final Softmax (21 classes)

>Input → MobileNetV2 → GAP → Dense(512) → Dropout → Dense(21) → Output


## Training Pipeline

1. Image loading + preprocessing  
2. Resize and normalize input  
3. Train/validation/test split  
4. Data augmentation  
5. Fine-tuning on MobileNetV2  
6. Evaluation using confusion matrix & metrics

## Results

- **Final Accuracy:** 94%
- **Epochs:** 15
- **Training Duration:** 2–3 hours per run (limited GPU)
- Strong class-wise performance

Performance visuals (to be added in repo):
✅ Accuracy/Loss curve  
✅ Confusion matrix  
✅ Sample predictions  

---

## Tech Stack

| Component | Tool |
|---------|-----|
| Language | Python |
| Framework | TensorFlow / Keras |
| Visualization | Matplotlib |
| Environment | Jupyter Notebook |
| Hardware | Limited GPU resources |


## Installation
pip install -r requirements.txt
