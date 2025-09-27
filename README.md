# 🚗 Automatic License Plate Recognition (ALPR)

This project is a **web-based application** for Automatic License Plate Recognition (ALPR).  
It allows users to upload an image of a vehicle, and the system will automatically:

- Detect the license plate  
- Segment the characters  
- Recognize the plate number using a **Convolutional Neural Network (CNN)**  

This application was developed as a project for the **CPE027 - Digital Signal and Processing** course.  

🔗 **Live Demo:** [ALPR Streamlit App](https://cpe027alpr-genonmurao.streamlit.app/)

---

## 👥 Authors
- **Genon, Twinkle S.**  
- **Murao, Christian Ivan P.**

---

## 🖼️ Screenshot
> Replace the placeholder below with a link to a screenshot of your running application.  

![App Screenshot](https://via.placeholder.com/800x400?text=Add+Project+Screenshot)

---

## ✨ Features
- **User-friendly Web Interface** – Interactive UI built with Streamlit  
- **Image Upload** – Supports `.jpg`, `.jpeg`, and `.png` formats  
- **Plate Detection** – Haar Cascade classifier locates the license plate  
- **Character Segmentation** – Contour analysis isolates characters  
- **Character Recognition** – TensorFlow/Keras CNN predicts characters  
- **Result Display** – Shows uploaded image and recognized plate number  

---

## 🛠️ Technology Stack
- **Backend:** Python  
- **Web Framework:** Streamlit  
- **Computer Vision:** OpenCV  
- **Deep Learning:** TensorFlow / Keras  
- **Data Handling:** NumPy  
- **Plotting:** Matplotlib  

---

## ⚙️ How It Works
The recognition pipeline consists of the following stages:

1. **Image Upload** – User uploads an image in the web interface  
2. **License Plate Detection** – `detect_plate` uses Haar Cascade (`indian_license_plate.xml`)  
3. **Preprocessing & Segmentation** – Resizing, grayscale conversion, thresholding, and morphological operations  
4. **Character Segmentation** – Contours matching character size are extracted and sorted left-to-right  
5. **Character Recognition** – Segments are passed into `predict_characters` using `Numberplate.h5` CNN model  
6. **Output** – Recognized characters are concatenated and displayed as the plate number  

---

## 🚀 Getting Started

### ✅ Prerequisites
- Python **3.8+**  
- pip (Python package installer)  

### 🔧 Installation

Clone the repository:
```sh
git clone https://github.com/your-username/CPE027_ALPR.git
cd CPE027_ALPR
