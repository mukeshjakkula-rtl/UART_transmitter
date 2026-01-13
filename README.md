**UART**
designed uart transmitter which can send the data at a speed of 1156000 symbols per seconds (baud_rate = 1156000).
Txclock = 50Mhz Tperiod = 20ns & data_width = 8bitswe calculate the error missmatch it is of +0.59% for Tx.

1/1156000 = 865.05ns is the time for each bit to stay on the tx_out line.

so accoding to the 50Mhz clock 50Mhz/1156000 = ~43 so each bit has to stay 43 clock cycles in tx_out line for 50Mhz clock.

so the actual baudrate is 50Mhz/43 = 1162790.

so the error between the intended baudrate and the generated baudrate is:

                 (1156000 - 1162790)/1156000 = +0.59% (good < 1%)


error of missmatch: 
