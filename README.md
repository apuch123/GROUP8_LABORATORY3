# GROUP8_LABORATORY3
The project initializes USART2 at 115 200 baud with 8 data bits, 1 stop bit, and no parity, then enables its global interrupt to handle character reception efficiently 
It uses HAL_UART_Transmit() in a one-second loop to repeatedly send the string “Hello from STM32!\r\n” over UART, allowing receipt confirmation via a PC terminal emulator 
Incoming characters are first polled with HAL_UART_Receive(), toggling an LED on ‘t’, then refactored to interrupt-driven reception with HAL_UART_Receive_IT(), storing bytes in a buffer and setting a flag for non-blocking processing in the main loop 
