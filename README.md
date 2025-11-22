# Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

## Aim:

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

## Apparatus Required: 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
## Theory:

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

## Algorithm:

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Programme:
```
import numpy as np
import matplotlib.pyplot as plt

Am = 11.4       
fm = 530     
Ac = 22.8       
fc = 5300     
fs = 53000     
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * 3.14 * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)
plt.title("Message Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
c = Ac * np.cos(2 * 3.14 * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)
plt.title("Carrier Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
df = 2000       
beta = df / fm
print("Modulation Index (β) =", beta)
s = Ac * np.cos(2 * 3.14 * fc * t + beta * np.sin(2 * 3.14 * fm * t))
plt.subplot(3,1,3)
plt.plot(t, s)
plt.title("Frequency Modulated Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.tight_layout()
plt.show()
```
## Tabulation:
![WhatsApp Image 2025-11-22 at 13 11 20_c584e534](https://github.com/user-attachments/assets/ce9a3ce8-e022-4a24-af15-459abafd2c8a)

## Output:
<img width="795" height="597" alt="Screenshot 2025-11-16 220249" src="https://github.com/user-attachments/assets/6b2ccf1d-d656-4bd2-9676-a72117bd3f4d" />

## Result:
Thus the frequency modulation (FM) using Python's NumPy and Matplotlib libraries is generated.
