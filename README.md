Project Overview

- This is a mock project to complete the internship at FPT Software Academy.

System Drivers

- Drivers for PCC, Systick, GPIO, UART, I2C, and RTC will be utilized, defined according to the documentation for the S32K144.

- Each function is being tested and works properly.

System Description


- The system includes a fingerprint sensor that recognizes which finger is pressed and compares it with the stored memory in flash. If a match is found, the name of the person is displayed on the LCD, and a buzzer is activated.

- Users can register a new fingerprint using a keypad.

Communication


- Communication between the LCD and the S32K is established via I2C.

- Communication between the AS608 fingerprint sensor and the S32K is conducted over UART.

- Communication between the keypad and the S32K is managed through GPIO.

Additional Information


- UART is used through openSDA for debugging purposes.

Limitations


- The system has a long delay time.

- The application does not utilize an operating system (OS); all operations are performed sequentially. If one module fails, the entire system may fail, making it difficult to identify which module is malfunctioning.

- The main function contains too much code, and the API functions are not specific to a single task.
