✋ Hand Gesture Recognition for Home Automation 🏠

📝 Project Description

This project implements a real-time hand gesture recognition system designed for home automation, particularly beneficial for individuals with speech impairments. The system uses computer vision and machine learning to detect hand gestures through a camera, classify them, and control home appliances via IoT integration.

✨ Key Features:

🖐️ Real-time hand detection using MediaPipe

🤖 Custom gesture classification with TensorFlow Lite

☁️ Adafruit IO integration for smart home control

🎯 94% accuracy in gesture recognition

♿ Designed for accessibility and ease of use

🛠️ Installation
📋 Prerequisites
Python 3.7+

pip (Python package manager)

📦 Dependencies

Install the required packages using:

bash
pip install --upgrade pip
pip install mediapipe numpy tensorflow opencv-python Adafruit-IO
🚀 Usage
🔧 Setup Adafruit IO:

Create an account at Adafruit IO

Create feeds for your devices (e.g., 'mode', 'r1s1', 'r2s1', etc.)

Update credentials in app.py:

python
ADAFRUIT_IO_USERNAME = 'your_username'
ADAFRUIT_IO_KEY = 'your_key'
🏃 Run the application:

bash
python app.py
👋 Gesture Controls:

The system starts in 'standby' mode

Show gesture combinations to control devices:

✌️ + 👍: Switch to 'detection' mode

✋ + ☝️: Control Relay 1 Switch 1

🖐️ + ☝️: Control Relay 1 Switch 2

✋ + ✌️: Control Relay 2 Switch 1

🖐️ + ✌️: Control Relay 2 Switch 2

🚪 Exit:

Press ESC to quit the application

📂 File Structure

hand-gesture-home-automation/
├── model/
│   ├── keypoint_classifier/
│   │   ├── keypoint_classifier.tflite  # 🧠 ML model
│   │   ├── keypoint_classifier_label.csv  # 🏷️ Gesture labels
│   │   └── keypoint.csv  # 📊 Training data
├── app.py  # 🚀 Main application
├── record.py  # 📹 Gesture recording
├── keypoint_classifier.py  # 🤖 Model wrapper
└── README.md  # 📖 This file
🎓 Training Custom Gestures

To add new gestures:

Run the recording script:

bash
python record.py
Press number keys (0-9) to label gestures

Collect 50-100 samples per gesture ✋

Retrain model with new data

📊 Performance
✅ Accuracy: 94%

⚡ Processing: 3s delay for stable recognition

👥 Supports multiple hand detection

🔌 Hardware Setup
Recommended components:

🍓 Raspberry Pi 400

📶 ESP8266 WiFi modules

🔌 Relay modules

📷 USB webcam

🤝 Contributing
Contributions welcome! Please:

🍴 Fork the repository

🌱 Create your feature branch

💾 Commit your changes

🔀 Push to the branch

🎯 Open a pull request


🙏 Acknowledgments

MediaPipe for hand tracking

TensorFlow Lite for efficient inference

Adafruit for IoT platform

❓ Support

For issues, please open an issue on GitHub. We're happy to help! 💬

