
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
% Define the discrete signal
n = 0:7;  % Time index
x = [1 2 3 4 4 3 2 1];  % Signal
N = length(x);  % Number of points in the signal

% Manually compute the DFT
X_dft_manual = zeros(1, N);  % Initialize the DFT result

for k = 0:N-1
    for n = 0:N-1
        X_dft_manual(k+1) = X_dft_manual(k+1) + x(n+1) * exp(-1j * 2 * pi * k * n / N);
    end
end

% Inverse DFT (IDFT)
x_idft_manual = zeros(1, N);  % Initialize IDFT result

for n = 0:N-1
    for k = 0:N-1
        x_idft_manual(n+1) = x_idft_manual(n+1) + (1/N) * X_dft_manual(k+1) * exp(1j * 2 * pi * k * n / N);
    end
end

% Compute the magnitude and phase from the manual DFT
amplitude_dft_manual = abs(X_dft_manual);
phase_dft_manual = angle(X_dft_manual);

% Plot amplitude and phase for manual DFT
figure;
subplot(2,1,1);
stem(0:N-1, amplitude_dft_manual, 'filled');
title('Amplitude Spectrum (Manual DFT)');
xlabel('Frequency index (k)');
ylabel('Magnitude');
grid on;

subplot(2,1,2);
stem(0:N-1, phase_dft_manual, 'filled');
title('Phase Spectrum (Manual DFT)');
xlabel('Frequency index (k)');
ylabel('Phase (radians)');
grid on;
```

**Output :**

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/ba413691-4575-4a26-b9d4-67309e5ddf59">
</p>


**8.4.3. DTFT & IDTFT :**
**Input :**

```matlab
% Define the discrete signal
n = 0:7;  % Time index
x = [1 2 3 4 4 3 2 1];  % Signal
N = length(x);  % Length of the signal

% Define frequency grid for DTFT
w = linspace(-pi, pi, 1000);  % Frequency axis (1000 points between -π and π)

% Compute the DTFT
X_dtft = zeros(1, length(w));  % Initialize the DTFT result
for i = 1:length(w)
    for n = 0:N-1
        X_dtft(i) = X_dtft(i) + x(n+1) * exp(-1j * w(i) * n);
    end
end

% Compute the magnitude and phase from the DTFT
amplitude_dtft = abs(X_dtft);
phase_dtft = angle(X_dtft);

% Plot the DTFT amplitude spectrum
figure;
subplot(3,1,1);
plot(w/pi, amplitude_dtft);
title('Amplitude Spectrum (DTFT)');
xlabel('Normalized Frequency (\times \pi rad/sample)');
ylabel('Magnitude');
grid on;

% Plot the DTFT phase spectrum
subplot(3,1,2);
plot(w/pi, phase_dtft);
title('Phase Spectrum (DTFT)');
xlabel('Normalized Frequency (\times \pi rad/sample)');
ylabel('Phase (radians)');
grid on;

% IDTFT (Reconstruction)
x_idtft = zeros(1, N);  % Initialize the IDTFT result
dw = w(2) - w(1);  % Frequency step size
for n = 0:N-1
    for i = 1:length(w)
        x_idtft(n+1) = x_idtft(n+1) + (1/(2*pi)) * X_dtft(i) * exp(1j * w(i) * n) * dw;
    end
end

% Plot the reconstructed signal using IDTFT
subplot(3,1,3);
stem(0:N-1, real(x_idtft), 'filled');
title('Reconstructed Signal (using IDTFT)');
xlabel('Time index (n)');
ylabel('Amplitude');
grid on;
```

**Output :**

<p align="center">

 <img  width="500" alt="image" src="https://github.com/user-attachments/assets/63e21e63-f0f4-423d-981d-94cc04fc7cb1">

</p>


**8.5. Discussion :**

<p text-align="justify">

 

</p>
 




