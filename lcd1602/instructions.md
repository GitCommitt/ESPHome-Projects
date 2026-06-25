# Steps to Build an ESP32-S3 with LCD Screen

To build this project, you will need the following hardware components:

### 1. ESP32-S3 Development Board
* **Specific board used in code:** `esp32-s3`
* **Features:** Make sure it has a USB-to-UART interface (like the USB_SERIAL_JTAG used in the logger configuration) for easy flashing via USB.

### 2. LCD1602 Display with I2C Backpack
* **Display size:** 16 characters by 2 rows (1602).
* **Interface:** It must have the black/blue I2C adapter board soldered to the back. This reduces the required data pins from 16 to just 2 pins (SDA and SCL).
* **Default Address:** Usually `0x27` (as configured in the YAML).

### 3. Jumper Wires
* **Type:** Usually 4x Female-to-Female jumper wires to connect the LCD backpack directly to the ESP32 pins.

### 4. USB Cable
* **Type:** USB-C cable (depending on your ESP32-S3 board) to power the device and flash the ESPHome firmware from your computer or Home Assistant server.

---

### Wiring Guide

Connect the 4 pins on the I2C backpack of the LCD1602 to the ESP32-S3 as follows:

| LCD1602 Pin | ESP32-S3 Pin | Description |
| :--- | :--- | :--- |
| **GND** | GND | Ground |
| **VCC** | 5V / VIN | Power  |
| **SDA** | GPIO 8 | Data Line |
| **SCL** | GPIO 9 | Clock Line |