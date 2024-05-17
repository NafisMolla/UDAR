# UDAR

![image](https://github.com/NafisMolla/UDAR/assets/37641864/eda7c527-bf8b-4f79-95b9-02693329be50)

![image](https://github.com/NafisMolla/UDAR/assets/37641864/4f4b2017-4c89-4752-93b1-5da9ff2445f6)

![image](https://github.com/NafisMolla/UDAR/assets/37641864/cf27a39a-e197-47c2-95c0-22a584b34c0e)




This project involves developing a gimbal system equipped with two servos for 360-degree movement and an ultrasonic sensor for distance measurement. The system supports manual and automatic operational modes, offering flexibility in control and functionality. In manual mode, users can directly control the gimbal's movement using a joystick. The joystick values are read via ADC channels, and the servos adjust accordingly to follow the user’s inputs, allowing for precise and responsive control over the gimbal's positioning.

In automatic mode, the gimbal continuously pans from one direction to the other. The ultrasonic sensor detects objects within its range. When an object is detected, the gimbal continues past it to mark the boundaries, then returns to the middle of the object, flashes the laser three times to indicate detection, and resumes panning. The system logs detected objects' angles, distances, and angular widths, and transmits this data via UART for display on a connected device.

The hardware components include an STM32 microcontroller, which manages the gimbal system and handles ADC, PWM, and UART operations; servos, which provide the mechanical movement for panning and tilting; an ultrasonic sensor for accurate distance measurement; a joystick for manual control; a laser for visual indication of object detection; and LEDs to indicate system status and operational mode.

The software components comprise ADC configuration for reading joystick values and ultrasonic sensor data, PWM configuration for precise servo control, UART communication for data transmission, and control logic for managing operational modes, object detection, and logging.

To use the system, ensure all hardware components are properly connected to the STM32 microcontroller and power up the system to initialize the peripherals. Use the provided button to toggle between manual and automatic modes, indicated by an LED. In manual mode, move the joystick to control the gimbal's position, with the servos following the joystick input. In automatic mode, the gimbal pans side to side, detecting objects and logging their details, which are transmitted via UART for display on a connected device.

Overall, this gimbal system provides versatile control and accurate distance measurement, making it suitable for applications requiring automated scanning and manual operation. Its ability to log and transmit data enhances its utility for monitoring and analysis tasks.
