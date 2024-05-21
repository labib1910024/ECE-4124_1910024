**4.1. Experiment No. :** 03

**4.2. Experiment Name :** Graphical representation of sampling, quantization using MATLAB.

**4.3. Theory :**

<p align="center">


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
 
