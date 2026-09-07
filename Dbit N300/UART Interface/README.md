The UART interface on the top of the board is the easiest place to start. 


<img width="3072" height="4080" alt="Flash Chip   UART" src="https://github.com/user-attachments/assets/e9efc59c-3f6c-43db-af4e-f8804ad8c28e" />


There are two main approaches when determining the baud rate: Use a signal analyzer and determine the exact baud rate, or guess common baud rates. I will walk through both.

**Calculating Baud Rates**

1. Hook up a logic analyzer to the UART interface, start your analysis software, and turn on the target device
2. Stop recording signals, go back to the start of the recording and measure the length of the signal. In our case, this is 26 microseconds
3. Do the following calculation: `1/26 x 1000` which equals `38.461`
4. This is very close to the common baud rate of `38400`, so we will use that when reading from UART

**Guessing Baud Rates**

Embedded systems usually use similar baud rates across different devices. If you don't have the patience for logic analysis, you can simply choose between these common baud rates and will likely find the correct one:

4800, 9600, 19200, 38400, 57600, 115200, 230400, 460800, and 921600
