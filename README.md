# NeuroRetina: Diabetic Retinopathy Severity Classification

NeuroRetina is a deep learning-based application designed to classify the severity of Diabetic Retinopathy (DR) using retinal fundus images. The project employs a Convolutional Neural Network (CNN) architecture optimized with image preprocessing techniques like CLAHE (Contrast Limited Adaptive Histogram Equalization) to improve diagnostic accuracy.

## 🚀 Features

- **Severity Classification**: Categorizes images into five stages of DR: No DR, Mild, Moderate, Severe, and Proliferative DR.
- **Image Preprocessing**: Implements CLAHE to enhance contrast in retinal images for better feature extraction.
- **Deep Learning Core**: Utilizes a custom 2D CNN architecture built with TensorFlow/Keras.
- **Web Interface**: Includes a Flask-based web application for user authentication and dashboard-based image uploads.

## 🛠️ Tech Stack

- **Languages**: Python
- **Deep Learning**: TensorFlow, Keras
- **Image Processing**: OpenCV (CV2)
- **Data Handling**: Pandas, NumPy
- **Web Framework**: Flask
- **Frontend**: HTML templates for Login, Registration, and Dashboard

## 📊 Dataset & Preprocessing

The model is trained on the **APTOS 2019 Blindness Detection** dataset.

- **Image Size**: All images are resized to 224 x 224 pixels.
- **Enhancement**: Images are converted to the LAB color space where CLAHE is applied to the L-channel before being converted back to RGB.
- **Augmentation**: Data is processed using a shuffled and batched TensorFlow Dataset pipeline.

## 🏗️ Model Architecture

The primary model is a 2D CNN consisting of:

- **Convolutional Layers**: Three blocks of `Conv2D` and `MaxPooling2D` layers with increasing filters (32, 64, 128).
- **Dense Layers**: A fully connected layer with 256 neurons and ReLU activation.
- **Regularization**: Dropout (0.5) to prevent overfitting.
- **Output**: A Softmax layer for 5-class classification.

## Project Structure
```
📁 Diabetic-Retinopathy-Severity-Classification
│
├── 📁 templates/                      # HTML templates for the web interface
│   ├── dashboard.html                 # User dashboard after login
│   ├── login.html                     # User login page
│   └── register.html                  # User registration page
│
├── .gitattributes                     # Git configuration attributes
├── app.py                             # Main Flask application file
├── cnn_model_1.h5                     # Trained CNN model for prediction
├── diabetic-retinopathy-final.ipynb   # Jupyter notebook for model training & evaluation
├── images.csv                         # CSV containing image paths and labels
├── train.csv                          # Training dataset metadata
└── README.md                          # Project documentation

```

## 💻 Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aditi380/diabetic-retinopathy-severity-classification.git
   cd diabetic-retinopathy-severity-classification
   ```
2. **Install dependencies:**Ensure you have Python installed, then run:

```bash
pip install tensorflow flask opencv-python pandas numpy
```

3. **Run the Flask App:**

```bash
python app.py
```

4. **Access the application:**
   Open your browser and navigate to http://127.0.0.1:5000/


