# 🛡️ Big Defend: ML-Powered Intrusion Detection System

Big Defend is an Intrusion Detection System (IDS) leveraging **Machine Learning** and **Real-Time Packet Capture**. It captures live network traffic using Scapy, trains an anomaly detection model (using scikit-learn), and monitors network activity for potential threats, presenting controls and logs via a sleek **GUI built with PySide6**.

---

## 🚀 Features

* ✅ **Live Packet Capture:** Captures real-time network traffic via Scapy.
* ✅ **ML-Powered Anomaly Detection:** Trains and utilizes a model to identify suspicious network patterns.
* ✅ **Real-Time Monitoring:** Actively runs the IDS to detect and log potential threats.
* ✅ **User-Friendly GUI:** Provides buttons to control IDS operations (Capture, Train, Start/Stop IDS) via a PySide6 interface.
* ✅ **Integrated Logging Console:** Displays live logs directly within the GUI.

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

1.  **Python:** Version **3.10 or higher**. Download from [python.org](https://www.python.org/downloads/).
    Verify your installation:
    ```sh
    python --version
    # or
    python3 --version
    ```
2.  **Git:** Required for cloning the repository. Download from [git-scm.com](https://git-scm.com/downloads).
3.  **uv:** A fast Python package installer and resolver used by this project. Installation instructions below.
4.  **Npcap (Windows Only):** **Mandatory for packet capture on Windows.** Scapy relies on Npcap to access network interfaces. Installation instructions below.

---

## 🏗️ Setup Instructions

These instructions are primarily for **Windows**. Setup on Linux or macOS may require different steps, particularly for packet capture dependencies (e.g., installing `libpcap-dev` on Debian/Ubuntu).

### Step 1: Install Npcap (Windows Requirement)

**Npcap is essential for packet capture functionality on Windows.**

1.  Download the latest **Npcap installer** from the official site: [Npcap Official Page](https://npcap.com/#download) (Successor to WinPcap).
2.  Run the installer. **Crucially, select the option during installation:**
    * ✅ Install Npcap in **WinPcap API-compatible Mode**.
3.  Complete the installation.
4.  **Restart your computer** to ensure Npcap is loaded correctly.

### Step 2: Install `uv`

`uv` is used for managing Python environments and dependencies efficiently. Open PowerShell and run:
```powershell
powershell -ExecutionPolicy Bypass -Command "irm [https://astral.sh/uv/install.ps1](https://astral.sh/uv/install.ps1) | iex"
```
*(Follow any prompts from the installer. You may need to restart your terminal or add `uv`'s directory to your PATH manually if it's not done automatically)*

### Step 3: Clone the Repository

```sh
git clone [https://github.com/adawatia/BigDefend.git](https://github.com/adawatia/BigDefend.git)
cd BigDefend
```

### Step 4: Install Python Dependencies

Use `uv` to install the required Python packages listed in the project's configuration (e.g., `requirements.txt` or `pyproject.toml`):
```sh
uv pip install -r requirements.txt
# or if using pyproject.toml without requirements.txt
# uv pip sync
```
*(Adjust the command based on your project's dependency file)*

---

## 🎯 Running Big Defend

**Note:** Packet capture typically requires **administrator privileges**. You may need to run your terminal or the application as an administrator.

### Option 1: Using the GUI (Recommended)

The GUI provides controls to manage the packet capture, model training, and IDS monitoring processes.

Start the GUI application:
```sh
uv run python gui.py
# Or potentially just `uv run gui.py` if configured in pyproject.toml
```
Use the buttons within the application to start/stop the different components. Logs will appear in the integrated console.

### Option 2: Running Components Manually (For testing/debugging)

You can run the individual scripts directly from your terminal:

* **Capture Live Network Traffic:**
    ```sh
    uv run python scripts/packet_capture.py
    ```
* **Train the IDS Model:**
    ```sh
    uv run python scripts/train_model.py
    ```
* **Start IDS Monitoring:**
    ```sh
    uv run python scripts/start_ids.py
    ```
* **Stop IDS Monitoring:** (If started manually or if GUI control is unavailable)
    ```sh
    uv run python scripts/stop_ids.py
    ```

---

## 🎨 GUI Overview

The **Big Defend** GUI features:

* A clear title with modern styling.
* Control Buttons: Start/Stop Packet Capture, Train Model, Start/Stop IDS.
* Integrated Console: Displays real-time logs from background operations.
* Contextual Controls: E.g., the "Stop IDS" button typically appears only when the IDS is active.

*(---screenshot of the GUI---)*
---

## 💡 Future Enhancements

* Improve IDS detection accuracy (e.g., explore deep learning models).
* Enhance GUI with a dashboard for visual analytics and statistics.
* Integrate cloud-based threat intelligence feeds.
* Support for additional network protocols and analysis techniques.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to fork the repository, make improvements, and submit a pull request. You can also open issues for bugs or feature suggestions.

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
