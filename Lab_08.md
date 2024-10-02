
**8.1. Experiment No. :** 08

**8.2. Experiment Name :**  Discussion about FFT,IFFT,DFT,IDFT,DTFT,IDTFT.

**8.3. Theory :**
<p text-align="justify">
 
</p>




**8.4. MATLAB Low pass filter representation using hamming window method :**
**8.4.1. FFT & IFFT :**
**Input :**

```matlab
% Define the discrete signal
n = 0:7;  % Time index
x = [1 2 3 4 4 3 2 1];  % Signal
N = length(x);  % Number of points in the signal

% Compute the FFT
X_fft = fft(x);  % Fast Fourier Transform (FFT)

% Compute the IFFT
x_ifft = ifft(X_fft);  % Inverse Fast Fourier Transform (IFFT)

% Compute the magnitude and phase from the FFT
amplitude_fft = abs(X_fft);
phase_fft = angle(X_fft);

% Plot amplitude and phase for FFT
figure;
subplot(2,1,1);
stem(0:N-1, amplitude_fft, 'filled');
title('Amplitude Spectrum (FFT)');
xlabel('Frequency index (k)');
ylabel('Magnitude');
grid on;

subplot(2,1,2);
stem(0:N-1, phase_fft, 'filled');
title('Phase Spectrum (FFT)');
xlabel('Frequency index (k)');
ylabel('Phase (radians)');
grid on;

% Plot the reconstructed signal using IFFT
figure;
stem(n, real(x_ifft), 'filled');
title('Reconstructed Signal (using IFFT)');
xlabel('Time index (n)');
ylabel('Amplitude');
grid on;
```

**Output :**

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/db6abf74-7743-456b-8ba6-3ac6e76100a8">

</p>

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/027240c5-21a3-4a52-83cd-39b3392fb5a0">

</p>



**8.4.2. DFT & IDFT :**
**Input :**

```matlab

```

**Output :**

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/a7cef53d-a2dd-4d38-bb73-554ee854c6dd">

</p>


**8.4.3. DTFT & IDTFT :**
**Input :**

```matlab

```

**Output :**

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/a7cef53d-a2dd-4d38-bb73-554ee854c6dd">

</p>


**8.5. Discussion :**

<p text-align="justify">

 

</p>
 




