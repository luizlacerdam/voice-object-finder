# 🎤📷 Voice-Activated Object Finder

This project is a real-time, voice-activated object detection app built with **Streamlit**, **YOLOv5**, and **speech recognition**. It uses your **computer's webcam** and microphone to detect spoken object names, then alerts you when those objects appear in the video feed.

---

## 🚀 Features

- 🎤 Voice recognition using Google Speech API
- 📷 Object detection using YOLOv5 (`yolov5s`)
- 🔊 Audio feedback using text-to-speech
- 🧠 Smart alias mapping (e.g. "phone" = "cell phone")
- 📜 Live detection logs
- 🔁 Frame skipping (processes every 3rd frame for performance)

---

## 🛠 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/voice-object-finder.git
cd voice-object-finder
```

### 2. Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

> 📌 If `requirements.txt` is not available, install manually:

```bash
pip install streamlit torch torchvision torchaudio opencv-python-headless pyttsx3 SpeechRecognition streamlit-webrtc
```

---

## ▶️ How to Run

Run the app using Streamlit:

```bash
streamlit run app.py
```

Then open the link shown in the terminal (e.g., `http://localhost:8501`) in your browser.

---

## 🧪 Notes

- Make sure your **microphone** and **webcam** are enabled in your browser.
- The app will detect objects using YOLOv5 on every 3rd frame for better performance.
- The detection log is saved in `detection_log.txt`.

---

## 📦 Folder Structure

```
├── app.py                 # Main Streamlit application
├── detection_log.txt      # Log of detected objects
├── venv/                  # Virtual environment (not committed)
└── README.md              # Project documentation
```

---

## 🤖 Model Info

This app uses [`ultralytics/yolov5`](https://github.com/ultralytics/yolov5) via `torch.hub` with the `yolov5s` variant (small and fast). You can switch to `yolov5n` for even faster detection or `yolov5m/l/x` for higher accuracy.

---

## 📃 License

MIT License. Feel free to modify and share!

---

## 🙌 Credits

Developed by [Your Name]. Uses YOLOv5 by Ultralytics, Streamlit for the UI, and Google Speech Recognition API.
