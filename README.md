# SynLingo Prototype ✨

An **Indian Sign Language (ISL) Detection Prototype** built using **MediaPipe Hand Tracking** and a clean, modern web UI.

This project demonstrates real-time hand tracking and basic gesture recognition directly in the browser.

---

## 🚀 Features

- 📷 Live camera feed
- ✋ Real-time hand tracking using MediaPipe
- 🧠 Basic gesture detection (Open Palm, Fist, Point, Pinch)
- ⚡ Smooth animations and responsive UI
- 🎨 Purple-blue metallic themed interface
- 🌐 Runs fully in browser (no backend required for demo)

---

## 🛠️ Tech Stack

- HTML, CSS, JavaScript
- MediaPipe Hands
- Canvas API

---

## 📦 API Integration (Roboflow)

You can connect this project to a trained ISL model using Roboflow.

### Node.js Example

Install dependency:

```bash
npm install axios
```

```js
const axios = require("axios");
const fs = require("fs");

const image = fs.readFileSync("YOUR_IMAGE.jpg", {
  encoding: "base64"
});

axios({
  method: "POST",
  url: "https://serverless.roboflow.com/indian-sign-language-detection/1",
  params: {
    api_key: "YOUR_API_KEY"
  },
  data: image,
  headers: {
    "Content-Type": "application/x-www-form-urlencoded"
  }
})
.then(res => console.log(res.data))
.catch(err => console.log(err.message));
```

---

## 💡 How It Works

1. Camera captures live video
2. MediaPipe detects hand landmarks (21 key points)
3. Simple logic classifies gestures
4. UI updates in real-time

---

## ⚠️ Note

- This is a **prototype**, not a full ISL translator
- For real accuracy, integrate a trained ML model (like Roboflow)
- Do **not expose API keys** in frontend apps

---

## 🧪 Future Improvements

- Full ISL alphabet detection
- Sentence formation
- Voice output
- Mobile optimization
- Model-based classification

---

## 👨‍💻 Developers

**Vishwajith, Drishti, Saumya, Manya**  
Class 11 AI Project

---

## 📄 License

This project is for educational purposes.
