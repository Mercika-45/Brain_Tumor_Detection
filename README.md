🧠 Brain Tumor Classifier
This project uses a Convolutional Neural Network (CNN) to classify brain MRI images into one of four categories:
glioma, meningioma, notumor, or pituitary.

It includes a Gradio interface for interactive image classification and supports dataset loading from Google Drive.

🔧 Features
🧠 Trained CNN on labeled MRI images

🚀 Deployed with Gradio web interface

📁 Reads dataset from Google Drive

🖼️ Image preprocessing and augmentation

📊 Multi-class classification with accuracy tracking

📁 Dataset Structure
Place your dataset inside Google Drive, structured like this:


/MyDrive/Training/
├── glioma/
├── meningioma/
├── notumor/
└── pituitary/
Each folder should contain relevant MRI images.

🧱 Dependencies
Install required libraries:

bash
Copy
Edit
pip install gradio opencv-python-headless tensorflow scikit-learn
If running in Google Colab, also mount your Drive:


from google.colab import drive
drive.mount('/content/drive')
🧠 Model Architecture
The CNN model includes:

3 Convolutional layers with ReLU

MaxPooling and BatchNormalization

Global Average Pooling

Fully Connected Dense layers with Dropout

Final Softmax output for 4-class prediction

🚀 How to Run
Mount Google Drive

python
Copy
Edit
from google.colab import drive
drive.mount('/content/drive')
Ensure Dataset Exists at /content/drive/MyDrive/Training.

Train the Model


model.fit(...)
Launch Gradio Interface


interface.launch()
🌐 Gradio Web App
Input: Upload an MRI image

Output: Predicted tumor type (glioma, meningioma, notumor, pituitary)

Confidence scores: Shown for all classes

📌 Notes
Training data is loaded once at the beginning

Model uses a basic CNN, suitable for educational or prototype use

Accuracy can be improved using transfer learning (e.g., VGG16, ResNet)
