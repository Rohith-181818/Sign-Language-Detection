# Sign-Language-Detection

🎯 Objective:
To develop a real-time system that recognizes hand gestures corresponding to common sign language words using a webcam. This system enables communication support for individuals with speech or hearing impairments.

⚙️ How It Works:
Hand Detection & Tracking:

Utilizes cvzone.HandTrackingModule (built on top of OpenCV and MediaPipe) to detect a hand in the video stream.

Extracts bounding boxes around hands for further processing.

Data Collection (datacollection.py):

Captures hand gesture images for various sign labels like “Yes”, “No”, “Hello”, “Thank You”, “I Love You”.

Images are stored in categorized folders under /Data/ for model training.

The hand is cropped, resized to a fixed dimension (300x300), and stored with uniform padding using OpenCV.

Model Training:

Although the training script is not included, the presence of keras_model.h5 and hands_model.h5 indicates the use of deep learning models trained using Keras.

Likely built with a Convolutional Neural Network (CNN) to classify the hand gesture images into one of the five predefined classes.

Prediction / Testing (test.py):

Uses the trained model (hands_model.h5) to classify new hand gestures in real-time.

Displays the predicted label over the live video feed.

Uses cvzone.ClassificationModule to simplify loading the model and running predictions.

📁 Data & Model Organization:
Data/ Folder:

Contains folders for each sign label (e.g., Yes, No, Hello, etc.)

Includes an additional Keras model (keras_model.h5) and labels.txt file for mapping output classes.

Model/ Folder:

Includes the final trained model (hands_model.h5) and its corresponding labels.

🧠 Technologies Used:
Component	Tool / Library
Hand Detection	OpenCV, cvzone, MediaPipe
Deep Learning	TensorFlow, Keras
Image Processing	OpenCV
Real-time Webcam Feed	OpenCV
Model Classification	cvzone Classifier
Programming Language	Python

💡 Features:
Real-time hand gesture recognition via webcam.

Custom sign dataset creation.

Simple model deployment with cvzone.

Recognizes multiple signs: Yes, No, Hello, Thank You, and I Love You.

🌐 Real-World Applications:
Assistive communication tools for hearing or speech-impaired individuals.

Educational tools to teach or learn sign language.

Human-computer interaction using gestures.

Accessible UI control via gestures in smart systems or IoT devices.

✅ Advantages:
Fully offline, no internet required during detection.

Can be extended by training with more gestures.

Lightweight and suitable for real-time usage on standard hardware.
