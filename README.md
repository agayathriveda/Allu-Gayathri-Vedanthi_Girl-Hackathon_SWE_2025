# Allu-Gayathri-Vedanthi_Girl-Hackathon_SWE_2025

Interpret.ai

Overview

Interpret.ai is an AI-driven text recognition tool that processes images and predicts textual content. The repository includes a trained deep learning model, dataset, and a graphical user interface (GUI) for easy interaction.

Installation

1. Clone the Repository

git clone <repository-url>
cd interpret.ai

2. Set Up a Virtual Environment

It is recommended to use a virtual environment to manage dependencies.

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

3. Install Dependencies

The following libraries are required for this project:

numpy

tensorflow

cv2 (OpenCV)

sklearn

gradio

os (built-in)

To install them, run:

pip install numpy tensorflow opencv-python scikit-learn gradio

Running the Project

1. Running in Google Colab

Since this project was developed in Google Colab, you need to:

Upload this repository to Google Drive.

Open model.ipynb in Colab.

Run the notebook cells sequentially.

2. Downloading the Dataset from Kaggle

To extract datasets from Kaggle, follow these steps:

!pip install kaggle
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d <dataset-name>
!unzip <dataset-name>.zip -d dataset/

GUI Structure

The GUI is implemented using gradio and provides a simple interface for users to upload an image and get text predictions.

Components:

Image Upload: Allows users to upload an image file.

Process Button: Runs the model and extracts text from the uploaded image.

Output Display: Shows the predicted text output.

Running the GUI

To start the GUI locally, run:

python gui.py

This will launch a web interface where users can interact with the model.

Project Structure

interpret.ai/
│── dataset/                   # Training dataset
│── model.h5                   # Trained deep learning model
│── classes.npy                 # Class labels
│── model.ipynb                 # Jupyter notebook for training/testing
│── gui.py                      # GUI application
│── requirements.txt            # Python dependencies
│── test_predictions_2.csv      # Sample test predictions

Notes

Ensure you have Python 3.7+ installed.

The dataset folder contains images and labels required for training.

If running on a GPU, ensure TensorFlow is configured correctly.
