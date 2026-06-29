# 🖼️ MNIST Image Denoising using Convolutional Autoencoder

## 📌 Project Overview

This project implements a **Convolutional Autoencoder** using TensorFlow and Keras to remove noise from handwritten digit images in the MNIST dataset.

An autoencoder is an unsupervised deep learning model that learns to compress an input image into a lower-dimensional representation (encoding) and reconstruct it back (decoding). In this project, the model is trained to reconstruct clean images from noisy inputs, effectively performing **image denoising**.

---

## 🎯 Objective

- Load the MNIST handwritten digit dataset.
- Add Gaussian noise to the images.
- Build a Convolutional Autoencoder.
- Train the model using noisy images as input and clean images as output.
- Reconstruct denoised images.
- Compare original, noisy, and reconstructed images.

---

## 📂 Dataset

**Dataset:** MNIST Handwritten Digits

- Training Images: 60,000
- Testing Images: 10,000
- Image Size: 28 × 28 pixels
- Number of Classes: 10 (0–9)

The dataset is automatically downloaded using TensorFlow:

```python
from tensorflow.keras.datasets import mnist

(x_train, _), (x_test, _) = mnist.load_data()
```

---

## 🛠️ Technologies Used

- Python 3
- TensorFlow / Keras
- NumPy
- Matplotlib

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/mnist-autoencoder.git
cd mnist-autoencoder
```

Install the required packages:

```bash
pip install tensorflow numpy matplotlib
```

---

## ▶️ Running the Project

Execute the Python script or Jupyter Notebook:

```bash
python autoencoder.py
```

or

```bash
jupyter notebook
```

Open the notebook and run all cells.

---

## 🧠 Model Architecture

### Encoder

```
Input (28×28×1)
        │
Conv2D (32 Filters)
        │
MaxPooling
        │
Conv2D (64 Filters)
        │
MaxPooling
        │
Encoded Representation
```

### Decoder

```
Encoded Representation
        │
Conv2D (64 Filters)
        │
UpSampling
        │
Conv2D (32 Filters)
        │
UpSampling
        │
Conv2D (1 Filter, Sigmoid)
        │
Output Image (28×28×1)
```

---

## ⚙️ Training Parameters

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Epochs | 15 |
| Batch Size | 128 |
| Noise Type | Gaussian Noise |
| Activation | ReLU, Sigmoid |

---

## 📊 Results

The model successfully learns to reconstruct clean handwritten digit images from noisy inputs.

The output consists of:

- Original Images
- Noisy Images
- Denoised Images

Training and validation loss decrease over epochs, indicating effective learning.

---

## 📈 Sample Output

```
Original Image
       ↓
Gaussian Noise Added
       ↓
Autoencoder
       ↓
Denoised Image
```

---

## 📁 Project Structure

```
MNIST-Autoencoder/
│
├── autoencoder.py
├── README.md
├── mnist_autoencoder.keras
├── requirements.txt
└── images/
    ├── original.png
    ├── noisy.png
    └── denoised.png
```

---

## 🚀 Future Improvements

- Train for more epochs to improve reconstruction quality.
- Experiment with different noise levels.
- Apply denoising autoencoders to CIFAR-10 or Fashion-MNIST.
- Explore Variational Autoencoders (VAEs).
- Implement image super-resolution using autoencoders.

---

## 📚 Learning Outcomes

Through this project, you will learn:

- Image preprocessing using TensorFlow
- Gaussian noise generation
- Convolutional Autoencoders
- Image denoising using deep learning
- Model training and evaluation
- Image reconstruction techniques

---

## 👨‍💻 Author

**Dinesh Jangir**

B.Tech (Computer Science Engineering)

Poornima University, Jaipur

---

## 📄 License

This project is developed for educational purposes as part of the Week 6 Deep Learning Assessment.