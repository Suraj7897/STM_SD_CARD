# **STM32 SD Card Interfacing** 🖥️💾  
### *Interfacing an SD card with the STM32F103C8T6 Blue Pill board using SPI communication*

---

## 📌 **Overview**  
In this project, we demonstrate how to interface an SD card with the **STM32F103C8T6 Blue Pill board** using **SPI communication**. This system can read/write files to the SD card, enabling data storage in embedded systems. The project uses the **FatFs file system** for managing files on the SD card. It is an excellent starting point for those looking to understand external memory interfacing with STM32.

---

## 🔥 **Features**  
- 🖥️ **SPI Communication**: Interfaces the SD card using the SPI protocol for high-speed data transfer.  
- 📁 **FatFs File System**: Implements a robust file system for managing data on the SD card.  
- 💡 **Simple Debugging**: Uses USB to Serial for easy debugging and monitoring of file operations.  
- 🛠️ **Modular Code**: Clean and structured code that is easy to modify for various uses.  
- 🚀 **Interchangeable STM32 Boards**: Although this project is based on the STM32F103C8T6 Blue Pill board, you can modify the code for other STM32 boards.

---

## 🛠 **Technologies Used**  
- **Hardware:**  
  - **STM32F103C8T6 Blue Pill Board**  
  - **SD Card Reader**  
  - **USB to Serial Converter** for debugging (FTDI, CP2102, etc.)  
- **Software:**  
  - **STM32CubeIDE** for code development  
  - **FatFs Library** for SD card file system management  
- **Communication Protocols:**  
  - **SPI** for SD card interfacing  
  - **UART** for debugging outputs  

---

## 🚀 **Getting Started**  
Follow these steps to set up the STM32 SD Card interfacing project on your board:

---

### **1. Prerequisites**  
- **STM32CubeIDE** (or another STM32 development environment)  
- **FatFs Library** (included in the project files)  
- **STM32F103C8T6 Blue Pill board** or other STM32 boards  
- **USB to Serial Converter** for debugging (optional, but useful for serial outputs)

---

### **2. Hardware Connections**  
#### **SD Card Connection (via SPI)**  
- **SD Card Reader** <--> **STM32F103C8T6**  
  - **VCC** → 5V  
  - **GND** → GND  
  - **CS** → PB12 (Port B 12)  
  - **SCK** → PB13 (Port B 13)  
  - **MISO** → PB14 (Port B 14)  
  - **MOSI** → PB15 (Port B 15)  

#### **UART Connection (for debugging)**  
- **USB to Serial Converter** <--> **STM32F103C8T6**  
  - **TX** → PA10 (Port A 10)  
  - **RX** → PA9 (Port A 9)

---

### **3. Installation**  
Clone the repository and configure your development environment:

``bash
git clone https://github.com/Suraj7897/STM_SD_CARD.git
cd STM_SD_CARD

4. Compiling and Flashing the Code
Use STM32CubeIDE (or your preferred tool) to compile the code and upload it to the STM32 board.

bash
Copy
Edit
# For STM32CubeIDE:
# Open the project in STM32CubeIDE and click 'Build' and 'Debug' to flash the code to the STM32 board.

# For other environments (e.g., PlatformIO or STM32CubeMX), follow the corresponding upload steps.
5. Testing the SD Card
Once the code is uploaded, the SD card will be automatically initialized, and you can monitor the file operations through the serial console. Files can be read/written to the SD card, and any errors will be shown in the serial debug window.

6. Code Structure
This project is structured into modular files for clarity:

fatfs_sd_card.c / fatfs_sd_card.h - Core files for initializing and interacting with the SD card using the FatFs library.
stm32_sd_card_config.c - Configuration for SPI, SD card, and UART peripherals.
main.c - Main logic for interacting with the SD card and debugging over UART.
usb_serial_debug.c - Handles serial communication for debugging outputs (optional).


7. Example Usage
Reading from SD Card: Once the system is running, files will be read from the SD card, and the data will be printed via UART for monitoring.
Writing to SD Card: The code supports writing data to files on the SD card using the f_write function from FatFs.
📸 Screenshots / Demo
Here are some screenshots of the setup and debug outputs during SD card operations:

![sdcard_2](https://github.com/user-attachments/assets/1cd358c7-be44-4ee7-991c-0cdb428547de)


Hardware setup with STM32F103C8T6 and SD card reader.

![sd_card_spi_1](https://github.com/user-attachments/assets/8dba61f3-6b54-4f30-853b-65ad7a4ccbf3)


Serial output showing SD card read and write operations.

![kwdvX](https://github.com/user-attachments/assets/a2b47cbc-7cd3-45a1-ad08-c3dc993d50d7)


🧑‍💻 Contributing
Feel free to fork this repository, submit issues, or create pull requests to improve the project. Contributions are welcome! 😊

🔗 Links
GitHub Repository: STM32 SD Card Interfacing


🎉 Thanks for exploring the STM32 SD Card Interfacing project! Expand your embedded system knowledge by working with external memory. 💾🖥️
