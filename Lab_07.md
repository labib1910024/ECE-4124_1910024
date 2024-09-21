
**7.1. Experiment No. :** 07

**7.2. Experiment Name :**  Z- transform ,inverse transform , poles and zeros by using MATLAB.

**7.3. Theory :**

<p text-align="justify">
  

</p>



**7.4. MATLAB Z-Transform representation :**

**7.4.1. Z-Transform  and Inverse transform of a Signal :**

**Input :**

```matlab
clc;
clear all;
close all;

% Parameters
fs = 1000;  % Sampling frequency (Hz)
f_cutoff = 150;  % Cutoff frequency for the low-pass filter (Hz)
N = 50;  % Filter order (adjust as necessary)

% Create a noisy signal (example)
t = 0:1/fs:1;  % Time vector (1 second)
signal = sin(2*pi*100*t);  % Original signal (100 Hz sine wave)
noisy_signal = signal + 0.5*randn(size(t));  % Add Gaussian noise

% Design the low-pass FIR filter using the Hamming window
normalized_cutoff = f_cutoff/(fs/2);  % Normalize cutoff frequency (0 to 1 scale)
b = fir1(N, normalized_cutoff, 'low', hamming(N+1));

% Apply the filter to the noisy signal
filtered_signal = filter(b, 1, noisy_signal);

% Plot the results
figure;
subplot(3,1,1);
plot(t, signal);
title('Original Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(3,1,2);
plot(t, noisy_signal);
title('Noisy Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(3,1,3);
plot(t, filtered_signal);
title('Filtered Signal (FIR with Hamming Window)');
xlabel('Time (s)');
ylabel('Amplitude');





```

**Output :**

<p align="center">

 
 <img  width="254px" alt="image" src=" ">


</p>


**7.5. Discussion :**

<p text-align="justify">


 

</p>
 



