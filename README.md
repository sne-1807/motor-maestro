# DC Motor Controller: Overview 
## Key Features
- **Microcontroller:** STM32F411CEU6 (STM32 Black Pill) with ST-Link
- **Closed-Loop Speed Control:** Utilizes an quadrature encoder for feedback from single motor to achieve accurate and stable motor speed using control algorithm (TBD)
- **Power Supply:** Can choose between a 12V Li-Po battery or DC jack as input, whic is stepped down using TPS5450 buck converter (12V to 5V) and further stepped down to 3.3V using a LDO (LP2985)
- **Motor and Driver:** 12V DC motor with rated torque of 0.25Nm and rated speed of 600RPM; Motor driver (DRV8874) in single H-bridge. Configured in PMODE = 0 (PH/EN Control Mode) and IMODE = Hi-Z (Fixed Off Time and Automatic Latched OFF in case of overcurrent)
- **Data Acquisition:** If required, can connect USB from microcontroller (STM32F407) to laptop to log data and plot PID curve etc
- **Speed Control and Display:** User adjustable speed control knob (rotary encoder for precision control) to manually vary motor speed, as well as GUI programmed into OLED Display to display real-time speed, as well as additional configurable motor settings

The design also includes other peripherals such as push-buttons for start/stop, E-Stop switch, and indicator LEDs for PWM, power, and fault detection. 
  
