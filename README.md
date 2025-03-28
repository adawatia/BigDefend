

# 🛡️ Big Defend

Big Defend is an advanced **Intrusion Detection System (IDS)** powered by **Machine Learning and Real-Time Packet Capture**. It captures live network traffic, trains an anomaly detection model, and monitors threats efficiently. The project comes with a sleek **GUI built using PySide**.

---

## 🚀 Features

✅ **Live Packet Capture** - Captures real-time network traffic using Scapy.  
✅ **Machine Learning Model** - Trains an IDS model to detect anomalies.  
✅ **Real-Time Threat Detection** - Runs IDS and logs suspicious activities.  
✅ **User-Friendly GUI** - Control IDS operations with a PySide6-based interface.  
✅ **Integrated Logging Console** - Displays live logs from background processes.  

---

## 🏗️ Setup Instructions (Windows)

### 🔹 Step 1: Install Required Dependencies

Ensure you have **Python 3.10+** installed. Download it from [Python's official site](https://www.python.org/downloads/).  

Check the installed Python version:
```sh
python --version
```

### 🔹 Step 2: Clone the Repository

```sh
git clone https://github.com/adawatia/BigDefend.git
cd BigDefend
```

### 🔹 Step 3: Install **Npcap** (Required for Packet Sniffing)

Big Defend uses **Scapy**, which requires **Npcap** to capture network packets.
1. Download **Npcap** from the official site: [Npcap Official Page](https://nmap.org/npcap/)
2. Run the installer and **select** the option:  
   - ✅ Install Npcap in **WinPcap API-compatible mode**.
3. Complete the installation and restart your computer.

### 🔹 Step 4: Install **uv**  

```sh
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## 🎯 Running the Application

### ✅ Start the GUI
```sh
uv run gui.py
```

### ✅ Capture Live Network Traffic
```sh
uv run scripts/packet_capture.py
```

### ✅ Train the IDS Model
```sh
uv run scripts/train_model.py
```

### ✅ Start IDS Monitoring
```sh
uv run scripts/start_ids.py
```

### ✅ Stop IDS Monitoring
```sh
uv run scripts/stop_ids.py
```

---

## 🎨 GUI Overview

The **Big Defend** GUI includes:
- **Cool Title Styling** with a modern font.
- **Buttons to Start/Stop Processes** (Packet Capture, Train Model, Start/Stop IDS).
- **Integrated Console Log** to display real-time logs from background processes.
- **Dynamic Visibility Control** - Only the "Stop IDS" button is visible when IDS is running.

---

## 🎯 Future Enhancements

🔹 Improve IDS detection accuracy with deep learning models.  
🔹 Enhance GUI with a **Dashboard for visual analytics**.  
🔹 Implement **Cloud-based threat intelligence integration**.  

---

## 🤝 Contributing

Want to contribute? Feel free to fork the repo and submit a pull request!

---

## 📜 License

This project is licensed under the **MIT License**.

---
