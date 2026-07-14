# 🌍 Automated Land Surface Temperature (LST), Lansat and Sentinel2 Mapping using Google Earth Engine & Python

An automated Python tool built with **Google Earth Engine (GEE)** and **Geemap** to dynamically compute and visualize monthly Land Surface Temperature (LST) over Sumatra, Indonesia. 

Instead of relying on pre-uploaded static assets, this script pulls live **Landsat 8 Top-of-Atmosphere (TOA)** data on-the-fly, processes thermal bands, converts the values to Celsius, and generates a standalone interactive HTML map that opens automatically in your browser.

---

## 🚀 Features

* **On-the-Fly Processing:** Filters and processes global USGS Landsat 8 data dynamically based on custom timeframes and Regions of Interest (ROI).
* **Thermal Analysis:** Converts Brightness Temperature from Band 10 ($B10$) from Kelvin to Celsius ($^\circ\text{C}$).
* **Dynamic Cloud Masking:** Filters out images with more than 30% cloud cover to ensure clean surface readings.
* **Auto-Export & Open:** Automatically saves the interactive visualization as an HTML file in the script's directory and opens it instantly in your default web browser.

---

## 🛠️ Prerequisites & Installation

Before running the script, ensure you have Python installed on your system. Open your Visual Studio Code (VS Code) terminal and complete the following steps:

### 1. Install Required Libraries
```bash
pip install earthengine-api geemap

### 2. Google Earth Engine Authentication
To use this script, you need a Google Earth Engine account. The first time you run the script, a browser window will pop up asking you to log in and grant access. It will provide an authentication token to paste back into your terminal.

💻 How to Run
Clone or download this repository.

Open the project folder in Visual Studio Code.

Open the Beginer_python_GBIF.py script.

Run the file using your Python interpreter:

Bash
python Beginer_python_GBIF.py
Wait for the terminal to print out the successful month-by-month compilation. Once finished, your default web browser will automatically pop up displaying the interactive map!

🗺️ Customization
You can easily modify the script constants inside Beginer_python.py to adapt it to your own research:

Change Region: Modify the coordinates lon, lat = 101.2853, -2.3432 to point to any location globally.

Change Timeframe: Adjust the year = 2023 variable or the target months array.

Adjust Heat Palette: Tweak the lst_vis dictionary to change the temperature range (min / max) or colors.

📦 Project Structure
├── Beginer_python_GBIF.py   # Main Python automation script
├── lst_temperature_map.html # Automatically generated interactive map
└── README.md                # Project documentation

🛠️ Built With
Google Earth Engine Python API - Cloud-based geospatial analysis platform.

Geemap - A Python package for interactive mapping with Google Earth Engine.
---
