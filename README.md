# **Digital Communications Project**
## - Using MATLAB, Communication toolbox
Simulating the performance of different modulation schemes:
- [**BPSK**](#binary-phase-shift-keying-modulation-bpsk)
- [**QPSK**](#quadrature-phase-shift-keying-modulation-qpsk)
- [**FSK**](#frequency-shift-keying-fsk)
- [**QAM**](#quadrature-amplitude-modulation-qam)
And add Additive White Gaussian Noise (AWGN environment) to evaluate the performance.

## Simulation Environment
These instructions for all the modulation schemes 
- Open MATLAB, then click on "Simulink", then click one "New Model"
- The simulation period is set to 10000. 
- Add these blocks: (to add just click with mouse then write the block name)
    * Random Integer: Sample Time = 1 s, Samples Per Frame = 100
    * "Name of modulator" Modulator Baseband
    * "Name of modulator" Demodulator Baseband
    * AWGN channel
    * Two Constellation Diagrams
    * Error rate calculation
    * Display
    * To workspace
- Make appropriate links between blocks (see the images)
- Open MATLAB command and write "bertool", Open MarleCarlo tab, Choose the write file
- Set BER diagrams to use a noise level of [-10, 10] dB (20 sample only).

Note: Scatter plots are produced at a noise level of 10 dB.
## **Binary Phase-Shift Keying Modulation (BPSK)**
### - Definition 
BPSK is modulation scheme makes the phase of the output signal gets shifted depending upon the input. It works on binary inputs, thus the output phase different is 180 degree.

### - Schema
```
- Random Generator set size = 2
```
![BPSK schema](/BPSK/BPSK-Digram.png)
### - Transmitter Scatter Plots (Before Noise)
![BPSK transmitter Before Noise](/BPSK/BPSK-BeforeNoise.png)
### - Receiver Scatter Plots (After Noise)
![BPSK receiver After Noise](/BPSK/BPSK-AfterNoise.png)
### - BER Plot
![BPSK BER Diagram](/BPSK/BPSK-BER.png)

___
## **Quadrature Phase-Shift Keying Modulation (QPSK)**
### - Definition 
QPSK is modulation scheme makes the phase of the output signal gets shifted depending upon the input. Exactly like BPSK but the input is 2-bits (4 values), thus the output phase will be shifted (0, 90, 180, or 270) degree.

### - Schema
```
- Random Generator set size = 4
- Phase offset (rad) = pi/4
``` 
![QPSK schema](/QPSK/QPSK-Digram.png)
### - Transmitter Scatter Plots (Before Noise)
![QPSK transmitter Before Noise](/QPSK/QPSK-BeforeNoise.png)
### - Receiver Scatter Plots (After Noise)
![QPSK receiver After Noise](/QPSK/QPSK-AfterNoise.png)
### - BER Plot
![QPSK BER Diagram](/QPSK/QPSK-BER.png)


___
## **Frequency Shift Keying (FSK)**
### - Definition 
FSK is modulation scheme makes the frequency of the output signal will be either high or low, depending upon the input data applied. The simplest FSK is binary FSK which I used here.

### - Schema
```
- Random Generator set size = 2
- M-ary number = 2
``` 
![FSK schema](/FSK/FSK-Digram.png)
### - Transmitter Scatter Plots (Before Noise)
![FSK transmitter Before Noise](/FSK/FSK-BeforeNoise.png)
### - Receiver Scatter Plots (After Noise)
![FSK receiver After Noise](/FSK/FSK-AfterNoise.png)
### - BER Plot
![FSK BER Diagram](/FSK/FSK-BER.png)

___
## **Quadrature Amplitude Modulation (QAM)**
### - Definition
QAM is modulation scheme makes the output signal get both ampltiude and phase shifting into a single channel, thereby it uses the bandwidth efficiently. It especially in wireless applications. Depending on number of symbols, another phases and amplitudes appear/disappear. 
For example:
- **QAM-4**: use two phases and two amplitudes.
- **QAM-16**: use four phases and four amplitudes.
- **QAM-64**: use eight phases and eight amplitudes.
I'll simulate QAM-16, and QAM 64 only.

### - Schema
```
- Random Generator set size = 16, 64
- M-ary number = 16, 64
- Normalization method = Average Power
- Phase offset (rad) = 0
- Average power referenced to 1 Ohm = 1 Watts
``` 

* **QAM 16**
![QAM16 schema](/QAM16/QAM16-Digram.png)
### - Transmitter Scatter Plots (Before Noise)
![QAM16 transmitter Before Noise](/QAM16/QAM16-BeforeNoise.png)
### - Receiver Scatter Plots (After Noise)
![QAM16 receiver After Noise](/QAM16/QAM16-AfterNoise.png)
### - BER Plot
![QAM16 BER Diagram](/QAM16/QAM16-BER.png)

* **QAM 64**
![QAM64 schema](/QAM64/QAM64-Digram.png)
### - Transmitter Scatter Plots (Before Noise)
![QAM64 transmitter Before Noise](/QAM64/QAM64-BeforeNoise.png)
### - Receiver Scatter Plots (After Noise)
![QAM64 receiver After Noise](/QAM64/QAM64-AfterNoise.png)
### - BER Plot
![QAM64 BER Diagram](/QAM64/QAM64-BER.png)

___
