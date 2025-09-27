# 📂 Code Folder – Smart Wellness Desk Assistant

This folder contains the STM32CubeIDE project source files for the **Smart Wellness Desk Assistant**, developed on the STM32 Nucleo-L476RG board.

---

## 📜 Files

### `main.c`
- Core application logic.  
- Implements:
  - User presence detection via ultrasonic sensor.  
  - Temperature monitoring using HW220 sensor (ADC).  
  - OLED display messages (I2C).  
  - Buzzer alerts after 1-hour sitting time.  
  - 30-second absence reset logic.  

---

### `stm32_hal_config.c`
- Handles **low-level hardware initialization**:
  - GPIO configuration (Ultrasonic, Temperature, OLED, Buzzer).  
  - Timer configuration (TIM1, TIM3, TIM4).  
  - NVIC interrupt setup.  

---

### `stm32_hal_config.h`
- Header file declaring initialization functions.  
- Keeps `main.c` clean by separating hardware configuration from application logic.  

---

## 🛠️ How to Use
1. Import this project into **STM32CubeIDE**.  
2. Ensure your board is set to **STM32 Nucleo-L476RG**.  
3. Flash the code to your STM32 board.  
4. Connect the peripherals as per the [Wiring Diagram](../Media/Wiring_Diagram.png).  
5. The system will run automatically on reset.  
