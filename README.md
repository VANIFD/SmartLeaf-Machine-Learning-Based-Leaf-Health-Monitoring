# SmartLeaf-Machine-Learning-Based-Leaf-Health-Monitoring


## Project Overview
**SmartLeaf** is a **Machine Learning** project that identifies whether a plant leaf is **healthy** or **diseased** using deep learning techniques.  
The project leverages a **Convolutional Neural Network (CNN)** to learn patterns from leaf images and classify new images in real time via a web application.  

This project demonstrates **supervised learning**, **image classification**, and **real-time prediction using ML**.  

---

## Features
- Predicts if a leaf is **Healthy** or **Diseased**  
- Shows **confidence scores** for predictions  
- Web-based interface for **easy image uploads**  
- Uses **data augmentation** to improve ML model generalization  
- Model saved in **Keras format** for easy deployment  

---

## Project Structure

plant/
├── data/ # Dataset folders
│ ├── train/ # Training images
│ │ ├── healthy/
│ │ └── diseased/
│ └── val/ # Validation images
│ ├── healthy/
│ └── diseased/
│
├── models/ # Trained model files
│ └── plant_disease_model.keras
│
├── src/ # Source code for training
│ └── train_model.py
│
├── web_app/ # Web application
│ ├── app.py
│ └── templates/
│ └── index.html
│
├── README.md # Project documentation
└── requirements.txt # Python dependencies


---

## Installation

1. Clone the repository:

```bash
git clone <your-repo-url>
cd plant

---

2. Create and activate a virtual environment

conda create -n env python=3.9
conda activate env

3. Install required packages:

pip install tensorflow flask numpy pillow scipy matplotlib

🚀 Training the Model

Ensure your training and validation images are in the correct folder structure (data/train, data/val).

Run the training script:

cd src
python train_model.py

🌐 Running the Web Application

Navigate to the web app folder:
cd ../web_app

Start the Flask server:
python app.py

Open your browser and go to:
http://127.0.0.1:5000

Machine Learning Details

Model Type: Convolutional Neural Network (CNN)

Input Size: 224 x 224 RGB images

Classes: Healthy (0), Diseased (1)

Loss Function: Binary Crossentropy

Optimizer: Adam

Data Augmentation: Rotation, zoom, horizontal/vertical flip

Training Method: Supervised learning on labeled images

💡 Notes & Tips

Use more images per class to improve accuracy.

Ensure validation images are different from training images to avoid overfitting.

Uploaded images should be similar in quality to training images for reliable predictions.

Transfer learning (MobileNetV2, ResNet50) can further improve performance on small datasets.

🔮 Future Improvements

Multi-class classification for different plant diseases

Add color-coded results and confidence thresholds in the web app

Enable real-time leaf detection via camera for field use


