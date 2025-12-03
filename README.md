# Traffic_Management
# AI-Based Traffic Management System

## 🚦 Overview
This project is an **AI-powered traffic signal controller** that dynamically adjusts green-light timing based on **vehicle density** detected from a live camera feed using **OpenCV**.

It uses:
- Background Subtraction (MOG2)
- Contour Detection
- Morphological Filtering
- Dynamic Time Calculation

This project simulates a real-world traffic control system using simple but effective Computer Vision techniques.

---

## 🧠 Features
- Real-time vehicle detection using webcam or video
- Counts vehicles in a single lane
- Dynamically adjusts signal time based on traffic load
- Lightweight (no deep learning required)
- Works on any normal PC with a webcam

---

## 📂 Project Structure
```
📁 Traffic-Management-AI
│── traffic.ipynb        # Jupyter notebook version
│── main.py              # Python script version
│── cars.xml             # Haarcascade vehicle detector (optional)
│── requirements.txt     # Dependencies
│── README.md            # Project documentation
```

---

## ⚙️ Installation
### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/traffic-ai.git
cd traffic-ai
```

### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the project
#### For Python script
```bash
python main.py
```

#### For Jupyter Notebook
Simply open `traffic.ipynb` and run all cells.

---

## 🔍 Working Principle
### Step-by-step workflow:
1. Capture frames from webcam
2. Convert to grayscale
3. Apply Background Subtraction (MOG2)
4. Threshold the mask to isolate moving objects
5. Dilate to remove noise
6. Find contours
7. Count vehicles based on contour area
8. Calculate dynamic green-light duration

---

## 🧮 Dynamic Signal Logic
```python
if vehicle_count < 3:
    green_time = 5
elif vehicle_count < 7:
    green_time = 10
else:
    green_time = 15
```

---

## 📸 Screenshot (Sample Output)
```
Vehicles: 5
Green Time: 10 sec
```
*(You can add actual images here once you upload to GitHub.)*

---

## ❗ Limitations
- Sensitive to lighting changes
- Errors if shadows or trees move
- Works for only one lane
- Cannot classify vehicles
- Not reliable for real-world deployment without deep learning

---

## 🚀 Future Improvements
- Use YOLOv8 for accurate vehicle detection
- Multi-lane detection
- Vehicle classification
- Database + dashboard for traffic analytics
- Deploy using edge devices (Jetson Nano)

---

## 🧑‍💻 Contributing
Pull requests are welcome. For major changes, open an issue first.

---

## 📜 License
MIT License. Free to use and modify.

---

## ⭐ Support
If you like this project, give it a ⭐ on GitHub!
