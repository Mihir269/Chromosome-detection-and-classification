# 🧬 Chromosome Detection and Basic Classification (Computer Vision Pipeline)

This project implements a **classical computer vision pipeline** for **chromosome detection** from microscopic images, followed by a **basic machine learning classification scaffold**.

The implementation is provided as a **Jupyter Notebook** and demonstrates:
- Chromosome segmentation using image thresholding
- Detection using contour extraction
- Feature extraction using resizing and flattening
- A placeholder **SVM-based classification setup**

⚠️ **Note:** The classification stage uses dummy labels and serves as a structural demonstration, not a biologically meaningful classifier.

---

## 🎯 Project Scope

The project focuses on:
1. **Detecting individual chromosomes** from a microscopy image
2. **Extracting regions of interest (ROIs)** using bounding boxes
3. **Preparing features** for downstream machine learning
4. Demonstrating how a **classifier can be trained** on extracted features

---

## 🧠 Methodology

### 1️⃣ Dataset Loading
- Dataset is downloaded from **Kaggle** using `kagglehub`
- Images are read directly from the downloaded directory

### 2️⃣ Image Preprocessing
- Convert RGB image to grayscale
- Apply **binary inverse thresholding** to separate chromosomes from background

### 3️⃣ Chromosome Detection
- External contours are extracted using OpenCV
- Each contour is assumed to correspond to a chromosome
- Bounding boxes are drawn and visualized

### 4️⃣ ROI Extraction
- Bounding rectangles are used to crop individual chromosomes
- Cropped chromosome images are stored for further processing

### 5️⃣ Feature Extraction
- Each chromosome ROI is resized to **64 × 64**
- Images are flattened into 1D feature vectors

### 6️⃣ Classification Scaffold
- Features are split into training and testing sets
- A **Support Vector Machine (SVM)** classifier is trained
- Labels are dummy (`all zeros`) and used only to demonstrate pipeline flow

---

## 🛠️ Technologies Used

- **Language:** Python  
- **Libraries:**
  - OpenCV
  - NumPy
  - Matplotlib
  - scikit-learn
- **Environment:** Jupyter Notebook / Google Colab
- **Dataset Source:** Kaggle

---

## 📂 Project Structure

```bash
.
├── InterIITTechAssignment_colabformat.ipynb   # Main notebook
├── README.md                                 # Project documentation
