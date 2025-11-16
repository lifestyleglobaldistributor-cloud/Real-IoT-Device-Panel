# Real-IoT-Device-Panel
Multi-Protocol Support
REST API - HTTP communication with devices
WebSocket - Real-time bidirectional communication
MQTT - (structure ready, requires Paho MQTT library)
📡 Live Features
Real-time sensor monitoring (polls every 2 seconds)
WebSocket live data streaming
Actual HTTP requests to device endpoints
Live device status updates
⚙️ Real Device Control
WiFi Configuration - Send actual credentials via POST /api/wifi/config
Network Scanning - Get available networks from device
OTA Firmware Updates - Upload binaries or use URLs with progress tracking
Custom Commands - Send any JSON payload to any endpoint
Working Endpoints Structure
The app expects your device to expose:
GET /api/status - Device info
GET /api/sensors - Sensor readings
POST /api/wifi/config - WiFi setup
POST /api/ota/update - Firmware update
POST /api/ota/upload - Binary upload
GET /api/ota/progress - Update progress
POST /api/system/reboot - Reboot device
POST /api/diagnostics - Run diagnostics
To Use With Real Devices:
For ESP32/ESP8266:
// Your device needs to implement REST endpoints like:
server.on("/api/status", HTTP_GET, handleStatus);
server.on("/api/sensors", HTTP_GET, handleSensors);
server.on("/api/wifi/config", HTTP_POST, handleWifiConfig);
Connection Examples:
REST: http://192.168.1.100 (your ESP32 IP)
WebSocket: ws://192.168.1.100:81
MQTT: ws://broker.hivemq.com:8000/mqtt
Just open the HTML file, enter your device's IP, and click Connect! 
