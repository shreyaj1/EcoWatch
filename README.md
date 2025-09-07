# ♻️ EcoWatch ✨  
**AI-based Waste Detection & Real-Time Alert Dashboard using YOLOv5**  

EcoWatch is a computer vision-based system to automate cleanliness monitoring across public spaces.  
It uses a custom-trained **YOLOv5** model to detect garbage in surveillance footage, trigger **real-time alerts**, and display actionable insights via an **interactive dashboard**.  

The project aims to ensure **hygiene, transparency, and accountability** within monitored environments.  

---

## 🧠 Key Features
- ⚙️ **Garbage Detection** using YOLOv5 (93% accuracy)  
- 🕵️ **Tracks Garbage** across frames with bounding boxes  
- 📩 **Real-time Alerts** via SMS & Email (Twilio API)  
- 📊 **Interactive Dashboard** for cleanliness and compliance monitoring  
- 🏆 **Ranking System** → evaluates sites based on compliance and response time  
- 👥 **Community Awareness** → encourage public participation in cleanliness drives  

---

## 🛠️ Project Workflow
1. **Image Acquisition**  
   - Surveillance footage captured from CCTV cameras.  
   - Frames processed using OpenCV → resized and passed into the YOLOv5 model.  

2. **Object Detection (YOLOv5)**  
   - Detects items such as bottles, boxes, cigarette butts, plastics.  
   - Applies **Non-Maximum Suppression (NMS)** to remove duplicates.  

3. **Model Execution (First-Time Setup)**  
   - Download and run `Launch AI Model.py` locally.  
   - Captures/accepts image input → runs inference → returns results.  
   - ✅ Local execution ensures privacy & reduces infra cost.  

4. **Garbage Tracking & Alerts**  
   - Persistent detections trigger automated alerts.  
   - SMS & Email notifications sent to authorities via **Twilio**.  
   - Dashboard updates with compliance status and proof-submission option.  

5. **Interactive Dashboard (React.js)**  
   - **Bar Charts**: frequency of garbage types  
   - **Line Charts**: trends over time  
   - **Pie Charts**: compliance scores  
   - **Interactive Map**: top vs. bottom performers  

6. **Community & Rankings**  
   - Highlights awareness initiatives.  
   - Sites ranked by response time, community involvement, and frequency of detections.  

---

## 📦 Tech Stack
| Layer        | Tools |
|--------------|-------------------------------|
| Frontend     | React.js, HTML, CSS, Recharts |
| Backend      | FastAPI / Flask, Firebase     |
| Notifications| Twilio API (SMS & Email)      |
| Mapping & UI | React Leaflet, Recharts       |
| CV Models    | YOLOv5, MIRNet (low-light)    |

---

## 📂 Repository Structure

<pre>
  EcoWatch/
├── backend/         # FastAPI/Flask backend for inference & alerts
├── frontend/        # React.js dashboard
├── models/          # YOLOv5 + MIRNet models (ONNX optimized)
├── data/            # Sample datasets
└── README.md        # Documentation
</pre>

---

## 📬 Contributing

We welcome contributions to EcoWatch!

Fork the repo

Create a branch (feature-xyz)

Commit changes & open a Pull Request 🚀

---

## 📜 License

This project is licensed under the MIT License.
