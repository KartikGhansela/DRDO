# DRDO
This project demonstrates a real-time Sign Language Recognition System that combines MediaPipe Holistic for human landmark detection and a Long Short-Term Memory (LSTM) deep learning model for temporal sequence classification. The goal is to move beyond single-frame gesture detection by capturing 30-frame sequences for accurate and smooth action recognition.

📌 Key Features
        MediaPipe Holistic Integration: Captures detailed 3D keypoints from the face, hands, and body for rich gesture representation.

        LSTM Neural Network: Utilizes a stacked LSTM model with dense layers to learn temporal patterns in sign language gestures.

        Real-time Detection: Runs live webcam input through the trained model to display gesture predictions with visual feedback and probability scores.

        Custom Dataset Collection: Captures and stores keypoints in organized folder structures for different actions, using NumPy arrays.

        Evaluation Tools: Includes confusion matrix and accuracy metrics for assessing model performance.

         Optimized Pipeline: Handles sequence stability, frame alignment, and false-positive filtering for reliable real-time prediction.

📁 Project Structure
          mediapipe_detection(): Preprocesses frames using MediaPipe and returns keypoints.

         draw_styled_landmarks(): Visualizes detected landmarks with custom styling.

         LSTM_Model(): A 3-layer LSTM model with 4 dense layers for multi-class classification.

         train.py: Script to train the model on collected data.

          real_time.py: Script to run the model in real-time with webcam feed.

🧠 Applications
    Sign language translation

    Gesture-controlled interfaces

    Assistive communication tools

    Human activity recognition

🚀 Technologies Used
   Python

   OpenCV

   MediaPipe

   TensorFlow / Keras

   NumPy, Matplotlib, Scikit-learn

Feel free to modify the architecture or add new gesture classes to expand this system! Perfect for beginners and researchers interested in computer vision, deep learning, and HCI (Human-Computer Interaction).


