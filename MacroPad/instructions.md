# Steps to Build an ESP32-S3 4-Key Macropad

To build this project, you will need the following hardware components:

### 1. ESP32-S3 Development Board
* **Specific board used in code:** `esp32-s3`
* **Features:** Make sure it has a USB-to-UART interface (like the USB_SERIAL_JTAG used in the logger configuration) for easy flashing via USB.

### 2. Mechanical Switches or Push Buttons
* **Quantity:** 4x momentary push buttons or mechanical keyboard switches (like Cherry MX or clones).
* **Interface:** Standard 2-pin contact switches.

### 3. Jumper Wires
* **Type:** Jumper wires (typically Female-to-Female or Female-to-Male depending on whether you use a breadboard) to connect the switches to the ESP32 pins.

### 4. USB Cable
* **Type:** USB-C cable to power the device and flash the ESPHome firmware from your computer or Home Assistant server.

### 5. 3D-Printed Case (Optional)
* **Type:** An additional 3D model is available to print an enclosure for the macropad to neatly house the electronics and switches.

---

### Wiring Guide

Connect one pin of each button to the designated GPIO pin on the ESP32-S3, and connect the other pin of all buttons together to a Ground (GND) pin:

| Component | ESP32-S3 Pin | Description |
| :--- | :--- | :--- |
| **Macropad Button 1** | GPIO 8 | Input Pin |
| **Macropad Button 2** | GPIO 9 | Input Pin |
| **Macropad Button 3** | GPIO 10 | Input Pin |
| **Macropad Button 4** | GPIO 11 | Input Pin |
| **All Buttons (Common)** | GND | Ground Connected in a line |