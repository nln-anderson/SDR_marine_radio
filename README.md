# Software-Define Marine VHF Radio
The goal of this project is to receive VHF marine radio signals using an RTL-SDR dongle, an antenna, and GNU radio.

## How It Works
It is easiest to understand how this works by stepping through each stage of signal.

The signal starts as an EM wave. For marine VHF channels, the frequency spectrum is from about 156MHz to 162MHz.
Each channel has a bandwidth of about 50kHz. The channel used in this project is channel 68, which operates at 156.425 MHz 
(so from 156.40 MHz to 156.450 MHz). These channels use frequency modulation for encoding information, and more specifically,
narrowband frequency modulation, since the bandwidth is only 25 kHz.

The signal reached the antenna of the receiver. From there, it goes through two processes. The first is the shift to an
analogue intermediate frequency (IF). After that, the IF signal is fed to a quadrature mixer where is is shifted to baseband frequency.

The diagram below shows how this all connects. 
![diagram](./images/RTL_SDR_architecture.png)
