**UART Transmitter**

This project implements a UART transmitter capable of sending serial data at a target baud rate of 1,156,000 symbols/second.

Design Parameters

TX clock frequency: 50 MHz

Clock period: 20 ns

Data width: 8 bits

Target baud rate: 1,156,000 bps

Bit Timing Calculation

The ideal time for one UART bit is:

1 / 1,156,000 ≈ 865.05 ns


With a 50 MHz clock:

50 MHz / 1,156,000 ≈ 43


Therefore, each bit is held on the tx_out line for 43 clock cycles.

Actual Generated Baud Rate
Actual baud rate = 50 MHz / 43 ≈ 1,162,790 bps

Baud Rate Error Analysis

The percentage mismatch between the intended and generated baud rates is:

(1,162,790 − 1,156,000) / 1,156,000 = +0.59%


A baud rate error of +0.59% is well within acceptable UART limits (typically < 1%), ensuring reliable data transmission.
