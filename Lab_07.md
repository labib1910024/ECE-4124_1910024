
**7.1. Experiment No. :** 07

**7.2. Experiment Name :**  Obtaining a linear phase FIR filter using Hamming/other types of window

**7.3. Theory :**

<p text-align="justify">
 An electric filter is a circuit that passes certain frequencies and rejects other frequencies. The simplest filters consist of two elements, RC and RL. A lowpass filter passes low frequencies and rejects high frequencies. A highpasss filter passes high frequencies and rejects low frequencies.
 
In signal processing, a finite impulse response (FIR) filter is a filter whose impulse response is of finite duration, because it settles to zero in finite time.

A Hamming window is a windowing function used in signal processing to concentrate the energy of a frame on the spectrum, reducing signal edge disparity by multiplying each frame with this specific function.

</p>



**7.4. MATLAB Low pass filter representation using hamming window method :**

**Input :**

```matlab
clc;
clear all;
close all;

fs = 1000; 
f_cutoff = 150;  
N = 50;  

t = 0:1/fs:1;  
signal = sin(2*pi*100*t); 
noisy_signal = signal + 0.5*randn(size(t));  


normalized_cutoff = f_cutoff/(fs/2);  
b = fir1(N, normalized_cutoff, 'low', hamming(N+1));


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

 
 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/a7cef53d-a2dd-4d38-bb73-554ee854c6dd">


</p>


**7.5. Discussion :**

<p text-align="justify">


 

</p>
 



