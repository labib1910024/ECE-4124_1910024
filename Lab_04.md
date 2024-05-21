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


</p>


**4.4. MATLAB Signal representation :**

**4.4.1. Sampling of a Signal :**

**Input :**

```matlab
%% sampling
t= 0:0.1:10;
y = sin(t);
stem(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Sin Signal');
grid on;

```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/e5308025-54fe-4d8d-a1c7-bbfc51e76ce8" height="400px" width="600px"/>
</p>



**4.4.2.  Signal :** 

**Input :**

```matlab

```

**Output :**

<p align="center">
 
  <img src="" height="400px" width="600px"/>
</p>



**4.4.3. Quantization of a Signal :** 

**Input :**

```matlab
%% Quantization
t = 0:0.1:10;
y = sin(t);
stem(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Sin Signal');
grid on;

num_bits = 4;


max_val = max(y);
min_val = min(y);
step_size = (max_val - min_val) / (2^num_bits); %formula
quantized_y = round(y / step_size) * step_size;


hold on;
plot(t, quantized_y, 'r', 'LineWidth', 1);
legend('Original Signal', 'Quantized Signal');
```

**Output :**

<p align="center">
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/f5efc8b3-bbf5-4862-93ca-a8ce50790600" height="400px" width="600px"/>
</p>


**4.5. Discussion :**

<p align="center">
  
 

</p>
 
