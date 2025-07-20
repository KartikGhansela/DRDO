# DRDO
Human Action Recognition using LSTM and MediaPipe. Captures 30-frame pose sequences to classify actions in real-time with high accuracy. Includes keypoint extraction, preprocessing, model training, and live prediction. Lightweight, fast, and ideal for gesture-based interfaces.
🧠 Human Action Recognition using LSTM Neural Networks
This project focuses on classifying human actions using a deep learning model based on Long Short-Term Memory (LSTM) networks. It takes in sequences of extracted features (like body keypoints or motion vectors) and learns temporal patterns to predict the performed action. The implementation is done in Python using TensorFlow and Keras, and includes TensorBoard support for visualizing model performance.

🔍 Overview
The system is designed to process time-series data, such as pose estimations over video frames. It uses stacked LSTM layers to learn from temporal features and dense layers to perform final classification. The model is trained on labeled sequences where each action is represented by a sequence of feature vectors.

📐 Model Architecture
Input Shape: Sequences of shape (30, 1662), representing 30 time steps and 1662 features.

LSTM Layers:

LSTM(64, return_sequences=True)

LSTM(128, return_sequences=True)

LSTM(64, return_sequences=False)

Dense Layers:

Dense(64, activation='relu')

Dense(32, activation='relu')

Output Dense layer with softmax for classification

📊 Training Insights
Loss Function: Categorical Crossentropy

Optimizer: Adam

Accuracy Achieved: ~98.8% categorical accuracy

Epochs: 150

Visualization: TensorBoard is used to track epoch_categorical_accuracy and loss.

The TensorBoard graph shows rapid improvement in accuracy within the first 50 epochs and then stabilizes, indicating effective learning with minimal overfitting.

📂 File Structure
train_model.py – Main training script

tensorboard_logs/ – Logs for real-time performance monitoring

model.png – LSTM architecture visualization

accuracy_plot.png – Accuracy trend during training

✅ Future Enhancements
Integrate MediaPipe for real-time pose extraction

Enable live webcam action prediction

Export model for mobile or edge deployment
