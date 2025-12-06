# Smart Prosthetic Leg with On-Device AI

This project, developed in collaboration with Bionic Soul, is an intelligent prosthetic leg that uses real-time sensor data and an on-device machine learning model to predict the user's intended knee angle. The project evolved from a cloud-based prototype to a highly efficient Edge AI solution.

## Key Features & Evolution

### Version 2: Edge AI Implementation (ESP32-S3)
This is the current, optimized version.
*   **On-Device Inference:** A `Decision Tree` model, trained in Python with Scikit-learn, was converted and deployed directly onto an **ESP32-S3 microcontroller**.
*   **Real-Time Performance:** The system captures data from an MPU6050 IMU, processes it through the local AI model, and controls a servo motor in real-time with very low latency.

### Version 1: Initial Prototype (Raspberry Pi)
*   **Data Collection:** An ESP32 collected data from IMU and force sensors.
*   **Centralized Processing:** The data was sent to a Raspberry Pi, which ran a `RandomForestRegressor` model in Python to perform the prediction.
*   **Mobile Interface:** A companion mobile app was developed in Flutter for device control and data visualization over BLE.

## Technologies Used

*   **Hardware:** ESP32-S3, MPU6050 IMU, Force Sensors, Servo Motor, Raspberry Pi 3.
*   **Firmware (C/C++): ESP-IDF, Arduino IDE.
*   **AI & Machine Learning:** Python, Scikit-learn (Decision Tree, RandomForest), Edge AI, TensorFlow Lite (for conversion).
*   **Mobile & Comms:** Flutter, Bluetooth Low Energy (BLE).
