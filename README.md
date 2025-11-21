# AM_Modulation_using_phython


Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing • Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

Under modulation : m<1, Em < Ec
Critical modulation: m-1, Em = Ec
Over modulation: m>1, Em > Ec
Note: Keep all the switch faults in off position

Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 4.9
fm = 384
Ac = 9.8
fc = 3840
fs = 38400
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```

Output Waveform
<img width="754" height="702" alt="image" src="https://github.com/user-attachments/assets/6df5d3a5-a9b0-492d-86d9-6483364e656e" />





Tabular Column

![WhatsApp Image 2025-11-21 at 10 58 40_6c810e62](https://github.com/user-attachments/assets/4e8d66c9-9da1-48e3-802b-2e1fbcfdbafa)



Calculation


ma (Theory) = am/ac = 6/12=0.5
ma(Practical) = (Emax-Emin)/(Emax+Emin) =12/24=0.5



Result


Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
