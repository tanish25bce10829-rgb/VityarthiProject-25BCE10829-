# 📝 Project Problem Statement & Scope

## 1. Problem Statement
In the logistics and e-commerce industry, accurate delivery time estimation is critical for customer satisfaction. However, many small businesses and independent couriers still rely on rough guesses or manual calculations that often overlook specific variables like vehicle type, vehicle speed limitations, and necessary handling/buffer time.

This lack of precision leads to:
* Unrealistic delivery promises to customers.
* Inefficient scheduling for delivery drivers.
* Increased friction between dispatchers and drivers.

There is a need for a lightweight, automated tool that can instantly calculate precise delivery estimates based on standard physics formulas ($Time = Distance / Speed$) while accounting for real-world operational delays.

## 2. Scope of the Project
The **Speed Logistics Calculator** is designed as a desktop-based simulation tool. 

### In-Scope (What the project DOES):
* **Speed Calculation:** Maps different vehicle types (Bike, Car, Drone) to their average operational speeds.
* **Physics Logic:** utilizes the fundamental formula $t = d/v$ to compute travel duration.
* **Operational Buffers:** Automatically incorporates fixed time buffers for parking, traffic, and package handling (set to 15 minutes).
* **User Interface:** Provides a graphical interface (GUI) for easy data entry without needing to write code.

### Out-of-Scope (What the project does NOT do):
* **Real-time Tracking:** The system does not use GPS or live Google Maps APIs.
* **Dynamic Traffic Updates:** It uses a static buffer for traffic, rather than real-time congestion data.
* **Database Integration:** It does not currently save the history of calculations to a database.

## 3. Target Users
* **Logistics Managers:** Who need to quickly estimate schedules for their fleet.
* **Small Business Owners:** Who manage their own local deliveries and need to give customers a time estimate.
* **Dispatchers:** Who assign vehicles to orders based on urgency and distance.

## 4. High-Level Features
* **Vehicle Speed Mapping:** The system intelligently selects speed parameters based on the chosen vehicle (e.g., limiting Bikes to 40 km/h vs. Drones at 100 km/h).
* **Detailed Time Breakdown:** Unlike standard calculators, this tool separates "Travel Time" from "Handover/Buffer Time," providing transparency in the final estimate.
* **Error Validation:** Includes input sanitation to prevent system crashes if users enter invalid text characters instead of numbers.
* **Modern Dark-Mode GUI:** A "Stark Industries" inspired interface using high-contrast colors (Dark Blue/Neon Green) to reduce eye strain and improve readability.
