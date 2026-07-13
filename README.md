# 🌍 Automated Land Surface Temperature (LST) Mapping using Google Earth Engine & Python

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
