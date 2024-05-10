**2.1. Experiment No. :** 02

**2.2. Experiment Name :** Forming time shifting,auto-correlation and cross-correlation of different types of signal using MATLAB.

**2.3. Theory :**

<p align="center">
  
Time shifting :

Time shifting is, as the name suggests, the shifting of a signal in time. This is done by adding or subtracting a quantity of the shift to the time variable in the function. Subtracting a fixed positive quantity from the time variable will shift the signal to the right that means delay by the subtracted quantity, while adding a fixed positive amount to the time variable will shift the signal to the left which means advance by the added quantity.

Auto correlation & cross correlation :

Sometimes auto correlation is known as serial correlation in the discrete time case, is the correlation of a signal with a delayed copy of itself as a function of delay. Informally, it is the similarity between observations of a random variable as a function of the time lag between them.

In signal processing, cross-correlation is a measure of similarity of two series as a function of the displacement of one relative to the other. This is also known as a sliding dot product or sliding inner-product. It is commonly used for searching a long signal for a shorter, known feature.


</p>


**2.4. MATLAB Signal representation :**

**2.4.1. Advancing of Signal :**

**Input :**

```matlab
clear all;
close all;
t1=-10;
t2=10;
N=5;
t=t1:t2;
y(t-N>0)=1;
y(t-N==0)=0;
y(t-N<0)=-1;

stem(t,y,'b','Linewidth',3);
xlabel('time');
ylabel('Amplitude');
title('Signum time Advanced Signal');

```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/e222d5e7-42a5-4369-9737-cff53be46613">
</p>




**2.4.2. Delaying of Signal :** 

**Input :**

```matlab
clear all;
close all;
t1=-10;
t2=10;
N=-5;
t=t1:t2;
y(t-N>0)=1;
y(t-N==0)=0;
y(t-N<0)=-1;

stem(t,y,'b','Linewidth',3);
xlabel('time');
ylabel('Amplitude');
title('Signum time Delayed Signal');
```

**Output :**

<p align="center">
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/b0f7b3c1-ed8a-4798-bac3-53aed76aea3c">
</p>



**2.4.3. Auto Co-relation & Cross-correlation :** 

**Input :**

```matlab
clear all;
close all;
t=-5:.5:5;
x1=sin(t);
x2=10*cos(t);

subplot(2,2,1);
plot(t,x1);
title('sin(t)');

subplot(2,2,2);
plot(t,x2);
title('5cos(t)');

subplot(2,2,3);
autocorr(x1);
title('Sample of autocorr');
subplot(2,2,4);
crosscorr(x1,x2);
title('Sample crosscorr');
```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/e74e33c3-bee7-4caf-b323-e4a245533226">
</p>



**2.5. Discussion :**

<p align="center">

Time shifting, auto-correlation, and cross-correlation are fundamental concepts in signal processing, widely used in various fields.
Time shifting, also known as time delay, refers to the process of shifting a signal in time. It's like moving the entire waveform along the time axis. This can be done by adding or subtracting a constant value to the time variable. Time shifting is often used to align signals or to study the effects of time delays in systems. For instance, in audio processing, time shifting can be used to synchronize multiple audio tracks. Here we use signum function for advancing and delaying the signal. We use user defined function and give some conditions on them , here we use the valude = 5 for advancing and delaying the signal.

Auto-correlation measures the similarity between a signal and a delayed version of itself as a function of the delay. It's essentially a measure of how much a signal correlates with a time-shifted version of itself. Here we use sine and cosine signal for the Auto-correlation.

On the other hand, Cross-correlation measures the similarity between two different signals as a function of the delay between them. It tells us how much one signal resembles another signal at different points in time.  Here we also use sine and cosine signal for the Auto-correlation.

In summary, time shifting, auto-correlation, and cross-correlation are essential tools for analyzing signals and data in different domains, helping us understand patterns, relationships, and dynamics over time. 

</p>
 

