# librtlsdr for 2-Frequency-Reception

## Description
Modified librtlsdr (*rtl_sdr* command) to enable seamless switching of frequency during reception.
This is based on the async_rearrangement branch of librtlsdr.

This lib enables TDOA localization with RTL-SDRs, when a reference transmitter is used for synchronization. More information:
<http://www.panoradio-sdr.de/tdoa-transmitter-localization-with-rtl-sdrs/>

## Usage
*rtl_sdr -f 200e6 -h 100e6 -n 1e3 record.dat*

receives first 1000 IQ samples at 200 MHz, then 1000 IQ samples at 100 MHz, then again 1000 at 100 MHz without interruption.

Type *./rtl_sdr* for help with the modified command.

## Build Instructions
1. navigate to main folder librtlsdr-2freq/
2. *mkdir build*
3. *cd build*
4. *cmake ../*
5. *make*

binaries can then be found in build/src/

DC9ST, 2017