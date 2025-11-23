# ⚡ Speed Logistics - Delivery Time Calculator

## 📖 Overview
**Speed Logistics** is a desktop application built with Python that helps logistics managers and users estimate delivery times based on distance and vehicle type. 

Unlike simple calculators, this tool provides a detailed breakdown of the total time, separating the actual travel physics from real-world buffer times (like traffic, parking, and handling). It features a modern, dark-themed Graphical User Interface (GUI) for a professional user experience.

## ✨ Features
* **Multi-Vehicle Support:** Calculate times for Bikes (40 km/h), Cars (60 km/h), and Drones (100 km/h).
* **Smart Physics Logic:** Uses the $Time = Distance / Speed$ formula for accurate travel estimates.
* **Real-World Buffers:** Automatically adds a 15-minute buffer for handling, packing, and traffic.
* **Detailed Breakdown:** Displays a "receipt-style" breakdown showing Travel Time vs. Handover Time.
* **Modern GUI:** A custom "Dark Mode" interface built with Tkinter, featuring hex-code styling and clean typography.
* **Error Handling:** Prevents crashes by validating that inputs are numbers, not text.

## 🛠️ Technologies & Tools Used
* **Language:** Python 3.x
* **Library:** Tkinter (Python's standard GUI library)
* **Editor:** VS Code

## ⚙️ Steps to Install & Run

### Prerequisites
Make sure you have Python installed on your system. You can check this by typing `python --version` in your terminal.

### Installation
1.  **Clone or Download** this repository to your local machine.
2.  Open the folder in **VS Code**.

### How to Run
1.  Open the **Terminal** in VS Code (Ctrl + `).
2.  Navigate to the project directory.
3.  Run the following command:
    ```bash
    python delivery_gui.py
    ```
    *(Note: If your file has a different name, replace `delivery_gui.py` with your filename).*

## 🧪 Instructions for Testing
Once the application window opens, try the following test cases to ensure it works correctly:

**Test 1: Short Distance (Bike)**
* **Distance:** `10`
* **Vehicle:** `Bike`
* **Expected Result:** * Travel: 15 mins
    * Handover: 15 mins
    * **Total:** 30 mins

**Test 2: Long Distance (Drone)**
* **Distance:** `100`
* **Vehicle:** `Drone`
* **Expected Result:** * Travel: 60 mins
    * Handover: 15 mins
    * **Total:** 75 mins

**Test 3: Invalid Input (Error Check)**
* **Distance:** `abc` (Type letters instead of numbers)
* **Vehicle:** Any
* **Expected Result:** A popup error message saying "Please enter a valid number."
