# IoT Sensor Data with ESP32, MongoDB, and Ubidots

## Overview
This project collects environmental data such as temperature, humidity, and motion using ESP32 with sensors. The data is then sent to a Flask API, stored in MongoDB Atlas, and visualized on Ubidots Dashboard.

## Features
- ESP32: Reads data from temperature, humidity, and motion sensors.
- Flask API: Handles incoming data from ESP32 and stores it in MongoDB.
- MongoDB Atlas: Cloud database to store sensor data.
- Ubidots Dashboard: Displays real-time sensor data.

## Setup Instructions
1. Prerequisites
   - ESP32 with sensors (DHT11 and PIR Motion Sensor)
   - Python 3 & Flask
   - MongoDB Atlas account
   - Ubidots account
2. Clone the repository
   ```
   git clone https://github.com/yourusername/iot-esp32-mongodb-ubidots.git
   cd iot-esp32-mongodb-ubidots
   ```
3. Set Up Flask API
   ### Install dependencies
   ```
   pip install -r requirements.txt
   ```
   ### Configure environment variables
   Create a .env file and add your MongoDB connection string:
   ```
   MONGODB_URI=mongodb+srv://your_username:your_password@cluster0.mongodb.net/?retryWrites=true&w=majority
   PORT=5000
   ```
   ### Run the Flask API
   ```
   python app.py
   ```
4. Flash ESP32 Code
   - Edit the ESP32 script (main.py for MicroPython)
   - Update WiFi credentials and API URL
   - Upload the code to ESP32
5. View Data on Ubidots Dashboard
   You can access the live dashboard at: [My Ubidots Dashboard](https://stem.ubidots.com/app/dashboards/public/dashboard/WCDegonwdB-SWfx6zCxxeOPIyroa4-R4nMgxFGXAQcg?navbar=true&contextbar=false)

## API Endpoints
| Method | Endpoint | Description |
| ------ | -------- | ----------- |
|  POST  | /api/data | Send sensor data |
|  GET  | /api/data | Retrieve stored data |
|  GET  | /health | Check API health status |

## Contributing
Feel free to fork this repository and submit pull requests!
   
   

