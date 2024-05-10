**1.1. Experiment No. :** 01

**1.2. Experiment Name :** Forming graph of different types of signal using MATLAB.

**1.3. Theory :**

<p align="center">
	
A signal is a source of information, generally a physical quantity, which varies with respect to time, space, temperature like any independent variable or A signal is a physical quantity that varies with time, space, or any other independent variable by which information can be conveyed. There are different types of signals. These are :
	
- **Unit step signal:** It often denoted as u(t), is essentially the output of the unit step function. It represents a signal that changes its value abruptly from zero to one at t=0, and remains at one for all 𝑡≥0.
  
- **Unit impulse signal:** The unit impulse signal, often denoted as 𝛿(𝑡), is a signal that represents an instantaneous burst or impulse of energy at t=0. It's also known as the Dirac delta function.
  
- **Ramp signal:** A ramp signal is a type of signal in which the amplitude varies linearly with time. The value is equal to time when 𝑡≥0 and value is 0 when t<0.
  
- **Parabolic signal:** A parabolic signal is a type of continuous-time signal whose amplitude varies quadratically with time. It represents the value t<sup>2</sup>/2  when  𝑡≥0 and values are equal to 0 when t<0.
  
- **Signum function:** The signum function, often denoted as sgn(𝑡) or sgn(𝑥), is a mathematical function that returns the sign of a real number 𝑥.
  
- **Exponential function:** A exponential signal is a type of signal whose amplitude varies exponentially with time. It is expressed as: x(t)= e<sup>αt</sup>
  
- **Rectangular signal:** It is also known as a square wave and is a type of signal that alternates between two constant amplitude levels over time. It is characterized by having equal durations of high and low states.
  
- **Triangular signal:** A triangular signal is a type of signal that varies linearly between two amplitude levels over time, forming a triangular shape when plotted against time.

</p>

**1.4. MATLAB Signal representation :**

**1.4.1. Unit Step Signal :**

**Input :**

```matlab
clear all; 
close all; 
t = -5:0.01:5; 
y(t>=0)=1; 
y(t<0)=0; 
plot(t,y,'b', 'LineWidth', 1); 
xlabel('Time');
ylabel('Amplitude');
title('Unit Step Signal'); 
```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/20a340a1-d37d-454c-aae0-29c4d2149937">
</p>


**1.4.2. Unit Impulse :** 

**Input :**

```matlab
clear all; 
close all; 
t = -5:0.01:5; 
y(t==0)=1; 
y(t>0)=0; 
y(t<0)=0; 
plot(t,y,'b', 'LineWidth', 1); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Unit Impulse Signal'); 
```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/c74fa2a2-a059-478f-8116-267121be6d0c">
</p>

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

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/f102617e-8c5f-4a35-90f1-a5d45df454eb">
</p>

**1.4.4. Parabolic Signal :**

**Input :**
```matlab
clear all; 
close all; 
t = -5:0.01:5; 
parabolic_signal = t.^2; 
plot(t, parabolic_signal,'b', 'LineWidth', 1); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Parabolic Signal'); 
 ```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/e588f766-2bed-454f-a8c5-e422f5ca52f6">

</p>


**1.4.5. Signum Function :**

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
signum_function = sign(t);
plot(t, signum_function,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude'); 
title('Signum Function'); 
```
**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/d341e3a0-4a9f-4465-beb7-f225b378f378">
</p>


**1.4.6. Exponential Signal :**

**Input :**
```matlab
clear all ;
close all;
t = -5:0.01:5;
a = 2;
b = 0.5; 
exponential_function = a * exp(b * t);
plot(t, exponential_function,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude'); 
title('Exponential Function'); 
 
```
**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/085e7a4e-dbba-46c8-b29e-bf2f87de5a26">
</p>


**1.4.7. Rectangular Signal :**

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
a = -2;
b = 2;   
rectangle_function = (t >= a) & (t <= b);
plot(t, rectangle_function,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude'); 
title('Rectangular Function'); 
```
**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/a10e31ca-c2e3-4a84-bf12-b8cb453939f1">
</p>

**1.4.8. Triangular Signal : ** 

**Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
period = 2;
amplitude = 1;  
triangular_waveform = amplitude * sawtooth(2*pi*t / period, 0.5);
plot(t, triangular_waveform,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude');
title('Triangular Waveform'); 

```
**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/ebf618a2-292a-4ecb-b0ee-6d8512386b40">
</p>


**1.4.9. Discrete Unit Step Signal Input :**
```matlab
clear all;
close all;
t = -5:0.01:5;
y(t>=0)=1;
y(t<0)=0;
stem(t,y,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude'); 
title('Unit Step Signal'); 
 ```
 
**Output :**
  
<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/19fa585b-b26b-4a38-972d-c9126976dab7">
</p>

 
**1.4.10. Discrete Unit Impulse ** 
**Input :** 
```matlab
clear all;
close all;
t = -5:0.01:5;
y(t==0)=1;
y(t>0)=0;
y(t<0)=0;
stem(t,y,'b', 'LineWidth', 1);
xlabel('Time');
ylabel('Amplitude'); 
title('Unit Impulse Signal');
```
 
**Output :** 

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/56b2433c-ea23-4a66-ac17-022fbc2c7ef2">
</p>
 
**1.4.11. Discrete Ramp Signal Input :**
```matlab
clear all; 
close all; 
t = -5:0.01:5; ramp_signal = t .* (t >= 0); 
stem(t, ramp_signal, 'b', 'LineWidth', 1); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Ramp Signal'); 
``` 
 
**Output :**
 
<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/77321cef-cd49-4427-83b3-8f1c082d6915">
</p>
 

**1.5. Discussion :**

<p align="center">

Forming signals in MATLAB is a fundamental aspect of signal processing and communications. MATLAB offers a wide range of functions and tools to create signals of different types, such as sine waves, square waves, triangular waves, impulse signals, and more. Here we use the condition and sometime use the functions for creating a signal. By using  sign() function , exp() function , sawtooth() function  for creating different types of sihnal such as : signum , exponential , sawtooth or triangular signal etc. Here we creating these signal respect to time .  With out using these default fuctions we can form themselves by using userdefined function and creating signals using various conditions on them.

</p>
