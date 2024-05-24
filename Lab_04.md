**4.1. Experiment No. :** 04

**4.2. Experiment Name :** Graphical representation of sampling, quantization using MATLAB.

**4.3. Theory :**

<p align="center">
  
Sampling :
  
To convert a signal from continuous time to discrete time, a process called sampling is used. The value of the signal is measured at certain intervals in time. Each measurement is referred to as a sample. The analog signal is also quantized in amplitude, but that process is ignored in this demonstration.

<p align="center">
<img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/ea2053eb-0f1d-46ce-a43c-4f0ae95d71ed" height="400px" width="600px"/>
</p>

Quantization:

Quantization in mathematics and digital signal processing, is the process of mapping input values from a large set to output values in a smaller set, often with a finite number of elements.

<p align="center">
<img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/13a8b5eb-c3b4-42c7-aa3e-ca438465ba5c" height="400px" width="600px"/>
</p>

Encoding

Signal encoding is the conversion from analog/digital data to analog / digital signal. In order to receive the signals correctly, the receivers bit intervals must correspond exactly to the senders bit intervals. The clock frequency of the transmitter and receiver should be the same.
</p>


**4.4. MATLAB Signal representation :**

**4.4.1. Sampling of a Signal :**

**Input :**

```matlab
%% sampling
t= 0:0.1:30;
y = 10* sin(t);

subplot(2,1,1);
plot(t, y,'b');
xlabel('Time');
ylabel('Amplitude');
title('Sin Signal');
grid on;

subplot(2,1,2);
stem(t, y,'r');
xlabel('Time');
ylabel('Amplitude');
title('Sampled Signal');
grid on;

```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/0f27298c-cddd-4882-a5f6-c18a6bafcbf9" height="400px" width="600px"/>

</p>



**4.4.2.  Signal :** 

**Input :**

```matlab
clear all;
close all;

f = 5; 
s_rate = 100; 
s_period = 1 / s_rate; 
max_time = 1; 

t_cont = linspace(0, max_time, 1000); 
t_sampled = 0:s_period:max_time;


s_cont = sin(2 * pi * f * t_cont); 
s_sampled = sin(2 * pi * f * t_sampled);


% Continuous signal
subplot(2, 1, 1); 
plot(t_cont, s_cont, 'b', 'LineWidth',2);
xlabel('Time (s)');
ylabel('Amplitude');
title('Continuous Signal');
grid on;

% Sampled signal
subplot(2, 1, 2); 
stem(t_sampled, s_sampled, 'r', 'LineWidth',2);
xlabel('Time (s)');
ylabel('Amplitude');
title('Sampled Signal');
grid on;

```

**Output :**

<p align="center">
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/565efa93-19dc-4f75-9a64-45d3a7b76f9f" height="400px" width="600px"/>

</p>



**4.4.3. Quantization of a Signal :** 

**Input :**

```matlab
clear all;
close all;
t = 0:0.1:15; 
y = 10 * sin(t);



subplot(2, 1, 1);
plot(t, y, 'b');
xlabel('Time');
ylabel('Amplitude');
title('Sine Signal');
grid on;


n = 4;
max_val = max(y);
min_val = min(y);
step_size = (max_val - min_val) / 2^n;

% Quantize the signal
quantized_y = round((y - min_val) / step_size) * step_size + min_val;


subplot(2, 1, 2);
stem(t, y, 'b');
xlabel('Time');
ylabel('Amplitude');
title('Quantized Signal');
grid on;
hold on;
plot(t, quantized_y, 'r', 'LineWidth', 1.5);

```

**Output :**

<p align="center">
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/b9295453-ef0c-4f52-9c3c-1aaf0f55c56d" height="400px" width="600px"/>
 
</p>


**4.5. Discussion :**

<p align="center">
  
 Here a signal is sampled in two ways. By using the stem function it is easy to plot at.
 
 ```matlab

stem()

```
The sampling frequency or sampling rate s_rate = 100 is the average number of samples obtained in one second that means samples per second thus s_period = 1 / s_rate. Then stem() function and plot is used to represent the graphical view. 

There is a formula for quantization of signal. Here number of bits = 4 .

```matlab

n = 4;
max_val = max(y);
min_val = min(y);
step_size = (max_val - min_val) / 2^n;

% Quantize the signal
quantized_y = round((y - min_val) / step_size) * step_size + min_val;



``

</p>
 
