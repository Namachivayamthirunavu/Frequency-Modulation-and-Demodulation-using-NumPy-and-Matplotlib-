## Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

### Aim:
To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.
### Apparatus Required:
1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer
### Theory:
Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.
### Algorithm:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

### Programme:
```
import numpy as np
import matplotlib.pyplot as plt
Am = 6.3
fm = 504
Ac = 12.6
fc = 5040
fs = 504000
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
efm = Ac * np.cos((2 * np.pi * fc * t) + 5.1 * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()
```
### Tabulation :
<img width="777" height="622" alt="image" src="https://github.com/user-attachments/assets/c0599e67-ddd4-4fb3-be65-50f1f0de0199" />

```
▲f  = Fmax – Fc
       = 8333.3 - 5000
       = 3333.3
ß = ▲f/Fm
   = 3333.3 / 494
   = 6.6

```

### Output:
<img width="630" height="469" alt="exp9 graph" src="https://github.com/user-attachments/assets/ab3f2773-b577-4709-b57d-cf17d3a32466" />

### Result:
The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. 
The modulated signal will show frequency variations corresponding to the amplitude of the message signal. 
