# ⚡ Speed Logistics - Advanced Delivery Time Estimator

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![GUI](https://img.shields.io/badge/Interface-Tkinter-green?style=flat)
![Status](https://img.shields.io/badge/Status-Active-orange)

> **A robust desktop utility for calculating precise logistics schedules using physics-based algorithms and operational variables.**

---

## 📑 Table of Contents
1. [About the Project](#-about-the-project)
2. [Key Features](#-key-features)
3. [Technical Architecture](#-technical-architecture)
4. [Project Directory Structure](#-project-directory-structure)
5. [Installation & Setup](#-installation--setup)
6. [How to Use](#-how-to-use)
7. [Testing & Validation](#-testing--validation)
8. [Future Roadmap](#-future-roadmap)
9. [Contact & Credits](#-contact--credits)

---

## 📖 About the Project

**Speed Logistics** is a solution designed to solve the problem of inaccurate delivery time estimation in local logistics. While map apps provide travel time based on traffic, they often fail to account for specific vehicle limitations and warehouse handling times.

This application serves as a **Decision Support System (DSS)** for dispatchers. It takes specific inputs (Distance and Vehicle Type) and processes them through a custom algorithm that combines:
1.  **Kinematics:** $Time = Distance / Speed$
2.  **Operational Overhead:** Fixed buffer times for packaging, labeling, and vehicle loading.

The result is a highly accurate "Total Delivery Time" displayed in a modern, high-contrast Dark Mode interface suitable for professional environments.

---

## ✨ Key Features

* **Multi-Modal Transport Support:**
    * 🚲 **Bike:** Optimized for short, urban trips (40 km/h).
    * 🚗 **Car:** Standard speed for medium-range deliveries (60 km/h).
    * 🚁 **Drone:** High-speed aerial delivery for urgent packages (100 km/h).
* **Granular Time Breakdown:** unlike simple calculators, this tool separates "Travel Time" (Physics) from "Handling Time" (Logistics), providing transparency.
* **Robust Input Validation:** The system employs `try-except` blocks to prevent crashes if a user inputs non-numeric characters.
* **Modern GUI (Dark Mode):**
    * Built with a custom color palette (`#2c3e50` Midnight Blue).
    * Uses Hex-code styling for a "Stark Industries" aesthetic.
    * Features high-readability fonts (Helvetica & Courier).

---

## ⚙️ Technical Architecture

This project is built using the **Event-Driven Programming** paradigm.

* **Language:** Python 3.10+
* **GUI Framework:** `tkinter` (Standard Python Interface to Tcl/Tk).
* **Logic:**
    * **Input Layer:** Captures raw strings from Entry widgets.
    * **Processing Layer:** Converts strings to floats, maps vehicle types to integer speeds, and computes time.
    * **Presentation Layer:** Formats the output string with newline characters (`\n`) for a receipt-style display.

---

## 📂 Project Directory Structure

When submitting your project, ensure your folder looks like this:


Speed-Logistics/
│
├── delivery_gui.py        # The main Python source code
├── README.md              # This documentation file

**Test 3: Invalid Input (Error Check)**
* **Distance:** `abc` (Type letters instead of numbers)
* **Vehicle:** Any
* **Expected Result:** A popup error message saying "Please enter a valid number."


Prerequisites
You must have Python installed. (Check by typing python --version in your terminal).

No external libraries (pip install) are required as tkinter is built-in.

Step-by-Step Guide
Clone or Download this repository to your local machine.

Open the folder in VS Code.

Open the integrated Terminal (Ctrl + ~).

Run the application using the following command:

Bash

python delivery_gui.py



🎮 How to Use
Launch: Run the script. A window titled "Speed Logistics" will appear.

Input Distance: Click the text box labeled "Destination Distance" and type the number of kilometers (e.g., 15.5).

Select Vehicle: Use the dropdown menu to choose your transport method (Bike, Car, or Drone).

Calculate: Click the red "CALCULATE ESTIMATE" button.

View Results: The green text area will show:

Travel Time (based on speed).

Handover Time (fixed 15 mins).

Total Estimated Time.




