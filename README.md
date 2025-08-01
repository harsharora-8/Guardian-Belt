## 📌 Overview

**Guardian Belt** is a wearable device that predicts and prevents falls in elderly individuals by leveraging motion sensors and machine learning. It aims to reduce the risk of injury and provide peace of mind to caregivers and families.

## 👴 Why It Matters

Falls are a leading cause of injury among the elderly. Many systems only detect falls *after* they happen. Guardian Belt goes one step ahead — it *predicts* a fall before it occurs, using real-time data and predictive algorithms.

## 🧠 Key Features

- 📊 Real-time motion monitoring using wearable sensors  
- ⚠️ Predicts potential falls before they occur using ML models  
- 🔔 Sends instant alerts via Google Apps Script (email/SMS)  
- 🔁 Continual learning and feedback loop  
- 🌐 Lightweight and portable — wearable as a belt or strap

## 🛠️ Tech Stack

**Hardware:**  
- MPU6050 (Accelerometer + Gyroscope)  
- ESP32 Microcontroller  
- Battery-powered belt-mounted prototype  

**Software:**  
- Python for data processing and ML  
- LightGBM, XGBoost, Random Forest models  
- Google Sheets as live cloud database  
- Google Apps Script for alerts  
- Arduino IDE for ESP32 firmware  

## ⚙️ How It Works

1. **Data Collection:**  
   Sensor data (acceleration, gyro) is collected via ESP32 and sent to Google Sheets.

2. **ML Prediction:**  
   Pre-trained models (Random Forest, XGBoost, LightGBM) analyze the data and flag risky movements.

3. **Real-Time Alerting:**  
   If fall risk is detected, alerts are triggered via Apps Script (email/SMS notifications).

4. **Logging:**  
   All data is logged for retrospective analysis and model improvement.

## 🧪 Models Used

- **Random Forest** – robust and interpretable  
- **XGBoost** – efficient and high-performing  
- **LightGBM** – optimized for speed and accuracy  

Each model's predictions are logged separately in a Google Sheet and compared for ensemble voting.

## 📁 Project Structure

- `/firmware/` – Arduino code for ESP32  
- `/ml-models/` – Jupyter Notebooks for training and predictions  
- `/scripts/` – Google Apps Script for triggering alerts  
- `/data/` – Sample training and testing datasets  

## 🚀 Getting Started

1. Clone the repository:
   git clone https://github.com/harsharora-8/GuardianBelt.git  
   cd GuardianBelt

2. Upload firmware to ESP32 using Arduino IDE

3. Set up Google Sheet and connect Apps Script for alerting

4. Run `predict.py` (or Jupyter Notebook) to fetch data and make predictions

5. Attach belt and start monitoring!

## 📊 Dataset

Custom sensor data collected using the Guardian Belt prototype.  
If you're replicating the system, you can generate your own labeled dataset or request sample data from this repo.

## 🛡️ Future Scope

- Add GPS tracking for fall location  
- Integrate heart rate or SPO2 sensors  
- Build mobile app dashboard  
- Use edge ML (TinyML) for on-device prediction  
- Collaborate with elderly homes/hospitals for pilot testing

## 🤝 Contributions Welcome!

- Fork the repo  
- Create a feature branch  
- Submit a pull request  
- Get reviewed and merged!

## 🙌 Acknowledgements

- Open-source contributors  
- Arduino and Google Apps Script community  
- Testers and mentors who helped validate the prototype

---

Built with 💙 to make aging safer through smart technology.
