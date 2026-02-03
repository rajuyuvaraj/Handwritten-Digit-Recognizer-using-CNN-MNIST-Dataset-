
# 🧠 Handwritten Digit & Multi-Digit Recognizer using CNN (MNIST)

This project implements a **Convolutional Neural Network (CNN)** using **TensorFlow/Keras** to recognize handwritten digits.
It starts with **single-digit recognition (0–9)** using the MNIST dataset and is **extended to recognize multi-digit numbers** (e.g., `1000`) from an image using **OpenCV-based digit segmentation**.

---

## 📌 Features

* ✅ Train a CNN on the MNIST dataset
* ✅ High accuracy (~99%) on test data
* ✅ Recognize **single handwritten digits**
* ✅ Recognize **multi-digit numbers** from an image
* ✅ Digit segmentation using OpenCV contours
* ✅ Visualize predictions and segmented digits

---

## 🛠️ Technologies Used

* **Python**
* **TensorFlow / Keras**
* **OpenCV**
* **NumPy**
* **Matplotlib**
* **Google Colab**

---

## 📂 Project Structure

```
Handwritten-Digit-Recognizer/
│
├── digit_recognizer.ipynb     # Main notebook
├── sample_images/
│   └── 1000.png               # Example multi-digit image
├── README.md                  # Project documentation
└── requirements.txt           # Dependencies
```

---

## 📊 Dataset

* **MNIST Dataset**

  * 60,000 training images
  * 10,000 test images
  * Grayscale images (28×28)
  * Digits from **0 to 9**

Loaded directly using:

```python
tf.keras.datasets.mnist.load_data()
```

---

## 🧠 CNN Model Architecture

```
Input: 28×28×1
↓
Conv2D (32 filters, 3×3) + ReLU
↓
MaxPooling (2×2)
↓
Conv2D (64 filters, 3×3) + ReLU
↓
MaxPooling (2×2)
↓
Flatten
↓
Dense (128) + ReLU
↓
Dense (10) + Softmax
```

---

## 🚀 Training Results

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Crossentropy
* **Epochs:** 5

**Test Accuracy:** ~99%

---

## 🔢 Multi-Digit Recognition Pipeline

1. **Upload Image** (e.g., `1000.png`)
2. **Convert to Grayscale**
3. **Invert Image** (MNIST style: white digits on black)
4. **Binary Thresholding**
5. **Find Contours** using OpenCV
6. **Segment Individual Digits**
7. **Resize to 28×28**
8. **Normalize & Predict each digit**
9. **Combine predictions into final number**

---

## 🖼️ Example Output

**Input Image:**
`1000.png`

**Segmented Digits:**
`[1] [0] [0] [0]`

**Final Prediction:**

```
Recognized multi-digit number: 1000
```

---

## ▶️ How to Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/Handwritten-Digit-Recognizer.git
cd Handwritten-Digit-Recognizer
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run Notebook

Open `digit_recognizer.ipynb` in **Jupyter Notebook** or **Google Colab** and run all cells.

---

## 📦 requirements.txt

```txt
tensorflow
opencv-python
numpy
matplotlib
```

---

## 🔮 Future Improvements

* 🔹 Support handwritten **sentences**
* 🔹 Use **CNN + LSTM** for sequence recognition
* 🔹 Improve segmentation for overlapping digits
* 🔹 Deploy as a **web app (Flask / Streamlit)**

---

## 👨‍💻 Author

**Raju Yuvaraj**
BCA Student | Machine Learning Enthusiast

---

## ⭐ Acknowledgements

* MNIST Dataset
* TensorFlow & Keras Documentation
* OpenCV Community

