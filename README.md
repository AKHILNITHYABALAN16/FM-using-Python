# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program

~~~~~~
import numpy as np
import matplotlib.pyplot as plt
Am = 5.3
fm = 424
Ac = 10.6
fc = 4240
fs = 424000
b = 4.3
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
efm = Ac * np.cos((2 * np.pi * fc * t) + 4.2 * np.sin(2 * np.pi * fm * t))
plt.figure(figsize=(10, 8))
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.title("Message Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.title("Carrier Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.title("FM Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.tight_layout()
plt.show()
~~~~~~

Output Waveform

<img width="1870" height="1011" alt="image" src="https://github.com/user-attachments/assets/1d60cbc9-119d-4f9d-ae87-d4914830c353" />

Tabular Column
![WhatsApp Image 2025-11-27 at 21 23 18_fdb78814](https://github.com/user-attachments/assets/77c1088e-448d-4732-afff-6485baf3e399)



Calculation


![WhatsApp Image 2025-11-27 at 21 23 19_33f0eee4](https://github.com/user-attachments/assets/505389d9-bd2d-402d-a68e-4815836bf3ea)


Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
