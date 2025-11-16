# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
// Parameters
Am = 11.1;        // Message amplitude
Fm = 500;         // Message frequency (Hz)
B  = 6.3;         // Modulation index
Ac = 22.2;          // Carrier amplitude
Fc = 5000;        // Carrier frequency (Hz)
Fs = 99000;       // Sampling frequency
T  = 0:1/Fs:2/Fm; // Time vector (two cycles of message)

// Message signal
em = Am * cos(2*%pi*Fm*T);
subplot(3,1,1);
plot(T, em);
xtitle("Message Signal");
xgrid();
// Carrier signal
ec = Ac * cos(2*%pi*Fc*T);
subplot(3,1,2);
plot(T, ec);
xtitle("Carrier Signal");
xgrid();
// FM signal
efm = Ac * cos( (2*%pi*Fc*T) + (B * sin(2*%pi*Fm*T)) );
subplot(3,1,3);
plot(T, efm);
xtitle("FM Signal");
xgrid();

Output Waveform
![WhatsApp Image 2025-11-10 at 23 07 38_1606ebb5](https://github.com/user-attachments/assets/3672d0f2-cbe2-48d1-abd4-2b3c7f07346f)



Tabulation

![WhatsApp Image 2025-11-16 at 14 03 12_94980075](https://github.com/user-attachments/assets/7b8ca72d-d4a2-475e-a9fb-d07fa8c430dd)


Calculation

![WhatsApp Image 2025-11-16 at 14 04 43_161d9e56](https://github.com/user-attachments/assets/aa60ec80-bf20-43d0-bf2d-5488a2dd07fc)


Frequency Deviation Practical = 20

Modulation Index Practical	= 2000

Modulation Index Theoretical	= 3900


RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


