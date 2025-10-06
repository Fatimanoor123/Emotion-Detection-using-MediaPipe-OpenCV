# 🎭 Emotion Detection using MediaPipe & OpenCV

This project detects **human emotions in real-time** using **MediaPipe FaceMesh** and **OpenCV**.  
It analyzes facial landmarks to classify simple emotions such as **Happy**, **Sad**, **Surprised**, and **Neutral**.

---

## 🧠 Project Overview

This project uses:
- **MediaPipe FaceMesh** for facial landmark detection (eyes, lips, etc.)
- **OpenCV** for image/video frame processing
- A custom rule-based classifier to determine emotion from facial features

It runs in **Google Colab** and saves the output video with detected emotions displayed on-screen in bold text.

---

## 🚀 Features

✅ Detects facial emotions in video files  
✅ Uses real-time FaceMesh landmark extraction  
✅ Displays the emotion name on screen in **large, dark text**  
✅ Saves the processed output video to **Google Drive**  
✅ Beginner-friendly — easy to extend with ML-based classifiers

---

## 📂 Folder Structure

```
Emotion-Detection-MediaPipe/
│
├── emotion_detection.ipynb     # Main Google Colab notebook
├── input_videos/               # Folder containing input videos
├── output_videos/              # Folder where processed videos are saved
└── README.md                   # Project documentation
```

---

## 🧩 Dependencies

Install the required libraries before running the notebook:
```bash
pip install opencv-python mediapipe numpy scipy
```

---

## 🧾 How It Works

1. **Load video** from Google Drive  
2. **Detect facial landmarks** using MediaPipe FaceMesh  
3. **Compute geometric ratios** (eyes, mouth, eyebrows)  
4. **Classify emotion** based on feature distances  
5. **Overlay detected emotion** text on the frame  
6. **Save the processed video** with emotion labels

---

## 💡 Emotion Logic (Rule-Based)

| Emotion     | Rule                                                                 |
|--------------|----------------------------------------------------------------------|
| **Happy**    | Mouth width ↑, mouth height ↑                                       |
| **Sad**      | Mouth narrow ↓, eyes slightly closed ↓                              |
| **Surprised**| Mouth height ↑↑, eyes wide open ↑↑                                  |
| **Neutral**  | No major change in facial geometry                                  |

---

## 🎥 Example Output

When the model processes a video, you’ll see text such as:
```
Emotion: Happy
```
<img width="552" height="887" alt="image" src="https://github.com/user-attachments/assets/6eff93fb-b132-4362-bb37-379d35506b2a" />

displayed clearly on the person’s face in large, dark text.

---

## 📁 Example Paths

Make sure to update the paths in your notebook before running:

```python
video_path = "/content/drive/MyDrive/AI ML Projects/Emotion-Detection/input/video1.mp4"
output_path = "/content/drive/MyDrive/AI ML Projects/Emotion-Detection/output/video1_output.mp4"
```

---

## 🧪 Future Work

- Add a CNN-based deep learning emotion classifier  
- Real-time webcam emotion recognition  
- Integration with sentiment-based alert systems  
- Emotion analytics dashboard for study or HR tools  

---

## 🧑‍💻 Author

**Fatima Noor**  
AI/ML Developer | Python Enthusiast  
📧 [GitHub Profile Link Here]  
📍 Based in Pakistan  

---

## 🪄 Inspiration

The project was inspired by how subtle changes in facial expressions reveal human emotions — bringing AI closer to understanding empathy.  
Built with ❤️ using **MediaPipe**, **OpenCV**, and **Python**.
