# Sign-Language-Translator
This project focuses on hand gesture recognition using computer vision and deep learning.
# Hand Gesture Recognition with Deep Learning

## 📁 Overview

This project is a complete pipeline for recognizing hand gestures using a webcam and deep learning. It includes:

- Dataset collection using real-time webcam feed
- Data augmentation for better generalization
- Model training using VGG16, ResNet50, and VGG19
- Evaluation and visualization of results

---

## 📂 Notebooks

### 1. Hands Detection - Dataset Creation.ipynb

📌 **Purpose:**  
Collect hand gesture images using your webcam and create a labeled dataset.

🔧 **Features:**
- Uses `cvzone`'s `HandDetector` to detect a single hand.
- Automatically crops, resizes, and centers the hand image to 300x300 px.
- Saves the original and 9 augmented images per gesture.
- Real-time preview of processed and cropped images.

👨‍💻 **How to Use:**
- Run the notebook.
- Enter a label name when prompted (e.g., `thumbs_up`, `stop`, `peace`).
- Press **`s`** to save an image (original + 9 augmented).
- Press **`q`** to quit.

---

### 2. Code Final.ipynb

📌 **Purpose:**  
Train a gesture classification model using preprocessed images.

🔧 **Key Steps:**
- Load and preprocess all images from labeled folders.
- Resize all images to 224x224 (suitable for VGG/ResNet).
- One-hot encode the labels.
- Split the dataset into training and testing sets.
- Train deep learning models (VGG16, ResNet50, VGG19).
- Evaluate and visualize accuracy and loss.

📊 **Outputs:**
- Model training curves
- Classification accuracy

---

## 🛠 Requirements

Install the following Python packages:

```bash
pip install tensorflow opencv-python numpy matplotlib scikit-learn pandas cvzone
