# 🎓 Classroom Attention Monitor

A real-time computer vision system to monitor and analyze student attention using webcam video. Designed for both **online** and **offline** learning environments, this tool leverages MediaPipe, custom-trained models, and feedback logging to detect 9 attention-related labels.

---

## 📌 Features

- ✅ Real-time webcam analysis
- 🧠 Multi-label attention detection (9 categories)
- 📉 Logs predictions to CSV
- 📊 Session analytics and feedback integration
- 📱 Phone usage and distraction detection
- 💤 Drowsiness detection via eye state
- 📸 Automatic edge case frame capture

---

## 🧠 Attention Labels

| Label               | Description                      | Works in         |
|---------------------|----------------------------------|------------------|
| Attentive           | Looking forward, engaged         | Online & Offline |
| Looking Away        | Head turned away                 | Online & Offline |
| Using Phone         | Holding phone, head down         | Online & Offline |
| Drowsy / Sleeping   | Eyes closed, head drooped        | Online & Offline |
| No Face Detected    | Not in frame or seat             | Online & Offline |
| Talking to Others   | Mouth and head turned            | Offline          |
| Fidgeting / Restless| Excessive motion                 | Online & Offline |
| Writing / Taking Notes | Looking down periodically     | Offline          |
| Engaged on Screen   | Minimal motion, focused          | Online           |

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/yourusername/classroom_attention_monitor.git
cd classroom_attention_monitor
```
### 2. Set Up Environment

```bash
pip install -r requirements.txt
```
Requires Python 3.8+ and packages like OpenCV, MediaPipe, scikit-learn, numpy, pandas, etc.

### 3. Directory Setup
Ensure these folders exist:

```bash

/data
/models
/logs
/src
```
Place:

Trained model → models/attention_model_realtime.pkl

Dataset CSV → data/attention_detection_dataset_v1.csv

### ⚙️ Run Real-Time Monitor
```bash
python src/realtime_monitor.py
Press q to quit the real-time view.
```
### 🧪 Train Your Own Model
```bash

python src/train_model.py
```
Make sure the dataset is labeled with the correct 9-label format.

### 🧩 File Structure
```css
📁 classroom_attention_monitor
├── models/
├── data/
├── logs/
├── src/
│   ├── train_model.py
│   ├── realtime_monitor.py
│   ├── utils.py
│   └── mediapipe_pose_face.py
├── requirements.txt
└── README.md
```
### 👨‍💻 Developer
Developed by Sankeerth Naidu
Guided by OpenAI's ChatGPT

### 📄 License
MIT License. Free for academic and research use.
