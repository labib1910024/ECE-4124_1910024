**1.1. Experiment No. :** 01

**1.2. Experiment Name :** Forming graph of different types of signal.

**1.3. Theory :**
A signal is a source of information, generally a physical quantity, which varies with respect to time, space, temperature like any independent variable or A signal is a physical quantity that varies with time, space, or any other independent variable by which information can be conveyed. There are different types of signals. These are :
	
- **Unit step signal:** It often denoted as u(t), is essentially the output of the unit step function. It represents a signal that changes its value abruptly from zero to one at t=0, and remains at one for all 𝑡≥0.
  
- **Unit impulse signal:** The unit impulse signal, often denoted as 𝛿(𝑡), is a signal that represents an instantaneous burst or impulse of energy at t=0. It's also known as the Dirac delta function.
  
- **Ramp signal:** A ramp signal is a type of signal in which the amplitude varies linearly with time. The value is equal to time when 𝑡≥0 and value is 0 when t<0.
  
- **Parabolic signal:** A parabolic signal is a type of continuous-time signal whose amplitude varies quadratically with time. It represents the value (t^2)/2  when  𝑡≥0 and values are equal to 0 when t<0.
  
- **Signum function:** The signum function, often denoted as sgn(𝑡) or sgn(𝑥), is a mathematical function that returns the sign of a real number 𝑥.
  
- **Exponential function:** A exponential signal is a type of signal whose amplitude varies exponentially with time. It is expressed as: x(t)= e^αt
  
- **Rectangular signal:** It is also known as a square wave and is a type of signal that alternates between two constant amplitude levels over time. It is characterized by having equal durations of high and low states.
  
- **Triangular signal:** A triangular signal is a type of signal that varies linearly between two amplitude levels over time, forming a triangular shape when plotted against time.



**1.4. MATLAB Signal representation :**

**1.4.1. Unit Step Signal :**

**Input :**

```matlab
clear all; 
close all; 
t = -5:0.01:5; 
y(t>=0)=1; 
y(t<0)=0; 
plot(t,y); 
xlabel('Time');
ylabel('Amplitude');
title('Unit Step Signal'); 
```

**Output :**

![photo_2024-05-07_22-22-53](https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/afbd8c8c-4b65-4c9e-8d2b-61b43445a99a)


**1.4.2. Unit Impulse :** 

**Input :**

```matlab
clear all; 
close all; 
t = -5:0.01:5; 
y(t==0)=1; 
y(t>0)=0; 
y(t<0)=0; 
plot(t,y); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Unit Impulse Signal'); 
```

**Output :**

**1.4.3. Ramp Signal :**

**Input :**
```matlab
clear all; 
close all; 
t = -5:0.01:5; 
ramp_signal = t .* (t >= 0); 
plot(t, ramp_signal, 'b', 'LineWidth', 2); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Ramp Signal'); 
```

**Output :**

**1.4.4. Parabolic Signal :**

**Input :**
```matlab
clear all; 
close all; 
t = -5:0.01:5; 
parabolic_signal = t.^2; 
plot(t, parabolic_signal); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Parabolic Signal'); 
 ```

**Output :**

**1.4.5. Signum Function :**

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
signum_function = sign(t);
plot(t, signum_function);
xlabel('Time');
ylabel('Amplitude'); 
title('Signum Function'); 
```
**Output :**

**1.4.6. Exponential Signal :**

**Input :**
```matlab
clear all ;
close all;
t = -5:0.01:5;
a = 2;
b = 0.5; 
exponential_function = a * exp(b * t);
plot(t, exponential_function);
xlabel('Time');
ylabel('Amplitude'); 
title('Exponential Function'); 
 
```
**Output :**

**1.4.7. Rectangular Signal :**

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
a = -2;
b = 2;   
rectangle_function = (t >= a) & (t <= b);
plot(t, rectangle_function);
xlabel('Time'); ylabel('Amplitude'); 
title('Rectangular Function'); 
```
**Output :**

**1.4.8. Triangular Signal : ** 

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
period = 2;
amplitude = 1;  
triangular_waveform = amplitude * sawtooth(2*pi*t / period, 0.5);
plot(t, triangular_waveform);
xlabel('Time');
ylabel('Amplitude');
title('Triangular Waveform'); 

```
**Output :**

**1.4.9. Discrete Unit Step Signal Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
y(t>=0)=1;
y(t<0)=0;
stem(t,y);
xlabel('Time');
ylabel('Amplitude'); 
title('Unit Step Signal'); 
 ```
 
**Output :**
  
 
 
**1.4.10. Discrete Unit Impulse ** 
**Input :** 
```matlab
clear all;
close all;
t = -5:0.01:5;
y(t==0)=1;
y(t>0)=0;
y(t<0)=0;
stem(t,y);
xlabel('Time');
ylabel('Amplitude'); 
title('Unit Impulse Signal');
```
 
**Output :** 
  
 
**1.4.11. Discrete Ramp Signal Input :**
```matlab
clear all; 
close all; 
t = -5:0.01:5; ramp_signal = t .* (t >= 0); 
stem(t, ramp_signal, 'b', 'LineWidth', 2); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Ramp Signal'); 
``` 
 
**Output :**
 
  
 



