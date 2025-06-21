# 🌿 Wild Medicinal Leaf Classification using CNN (MobileNetV2)

A deep learning-based image classification project that identifies 21 species of wild medicinal leaves using convolutional neural networks and transfer learning. This project uses MobileNetV2 to build an efficient, accurate model, with extensive data augmentation and class balancing.

---

## 📁 Project Structure

WILD-MEDICINAL-LEAF-CLASSIFICATION/
├── balanced_medicinal_plant/ # Final dataset used for training (after augmentation)
├── model/ # Saved model or checkpoints
├── WILD MEDICINAL LEAF CLASSIFICATION USING CNN.ipynb
├── README.md
└── requirements.txt

---

## 🔍 Problem Statement

Medicinal plant classification is vital for biodiversity conservation, ethnobotany, and pharmaceutical applications. Manual classification is error-prone and time-consuming. The aim is to **automate the identification** of medicinal leaves using a CNN-based image classification model.

---

## 📊 Dataset Overview

- 📷 **Total Classes:** 21 wild medicinal leaf species
- 🧠 **Balanced:** Each class has ~400 images after augmentation
- 💡 **Image Size:** Resized to 224x224 pixels
- 📂 **Train/Validation Split:** 80% training / 20% validation

---

## 🛠️ Tools and Technologies

- Python
- TensorFlow / Keras
- MobileNetV2 (Transfer Learning)
- ImageDataGenerator (Augmentation)
- NumPy, Matplotlib, scikit-learn

---

## 🔄 Data Preprocessing & Augmentation

- Rescaling pixel values (1./255)
- Rotation, shear, zoom, brightness adjustments
- Horizontal flip
- Class balancing via manual augmentation
- Data loaded using `flow_from_directory` with `subset='training'/'validation'`

---

## 🧠 Model Architecture

- 📦 **Base Model:** MobileNetV2 (pretrained on ImageNet, frozen)
- 📐 **Custom Layers:**
  - GlobalAveragePooling2D
  - Dense(512, ReLU) with L2 regularization and Dropout
  - Output layer: Dense(21, Softmax)
- 🔧 **Loss Function:** Categorical Crossentropy
- 🎯 **Optimizer:** Adam (lr = 0.0005)
- 🧮 **Metrics:** Accuracy

---

## ⚖️ Class Weighting

To handle any class imbalance, class weights were computed using `sklearn.utils.compute_class_weight`.

---

## 📈 Training Strategy

- ✅ 50 Epochs
- ✅ Batch Size: 64
- ✅ Learning Rate Scheduler (Decay after 5 epochs)
- ✅ Class Weights
- ✅ Early Stopping and ModelCheckpoint (optional to add)
- ✅ Evaluation using classification report & confusion matrix

---

## 📊 Results

| Metric           | Value            |
|------------------|------------------|
| Training Accuracy | ~XX.XX% |
| Validation Accuracy | ~XX.XX% |
| Best Model | MobileNetV2 (frozen base) |
| Number of Classes | 21 |
> (Replace with your actual values)

---

## 📌 Key Takeaways

- Transfer Learning is powerful for small, domain-specific datasets.
- Data augmentation and class balancing greatly improved performance.
- Lightweight models like MobileNetV2 are fast and efficient, even on lower-end machines.

---

## 📂 How to Run

```bash
# Clone the repo
git clone https://github.com/<your-username>/wild-medicinal-leaf-classification.git
cd wild-medicinal-leaf-classification

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook
