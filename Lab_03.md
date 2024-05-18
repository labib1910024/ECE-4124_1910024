**3.1. Experiment No. :** 03

**3.2. Experiment Name :** Convolution and Cross correlation with function and tebular format using MATLAB.

**3.3. Theory :**

<p align="center">
  
Convulation :
Convolution is a mathematical way of combining two signals to form a third signal. It is the single most important technique in Digital Signal Processing. Using the strategy of impulse decomposition, systems are described by a signal called the impulse response. By using matlab we can do it in two ways. Such as : Function & Tabular Format. Here is a default function in MATLAB for convulation. If there is two  array and they are distributed in two sides of the table and multiply them am add them as like as the below figure.
<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/f16c0d28-e27b-4fed-b450-b466ac56ebe0" height="200px" width="400px"/>
</p>


Cross correlation :
In signal processing, cross-correlation is a measure of similarity of two series as a function of the displacement of one relative to the other. This is also known as a sliding dot product or sliding inner-product. It is commonly used for searching a long signal for a shorter, known feature. Here is also by using matlab we can do it in two ways. Such as : Function & Tabular Format. Here is a default function in MATLAB for convulation. If there is two  array  .At first flip the one signal and they are distributed in two sides of the table and multiply them am add them as like as the above figure. It is same as the convulation but flip the one array first.

</p>


**3.4. MATLAB Signal representation :**

**3.4.1. Convulated Signal :**

**Input :**

```matlab
%% convoluted signal with tebulated method & function

clc
clear all;
close all;

a=0:1:4;
x=[1 2 3 1 2];
y=[1 -1 1 1 -1];
z=conv(x, y);
n2=0:length(z)-1;

la=length(x);

lb=length(y);
ind=la+lb-1;

con_sig=zeros(1,ind);
b=0:length(con_sig)-1;

for i=1:ind
    for j=1:lb
        if (i-j+1)>0 && (i-j+1) <=la
            con_sig(i)=con_sig(i)+y(j)*x(i-j+1);
        end
    end
end

figure
subplot(4,1,1)
stem(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Signal-01');
grid on;


subplot(4,1,2)
stem(a,y);
xlabel('Time');
ylabel('Amplitude');
title('Signal-02');
grid on;

disp(con_sig)
subplot(4,1,3)
stem(con_sig);
xlabel('Time');
ylabel('Amplitude');
title('Convolution with tabular format');
grid on;

subplot(4,1,4);
stem(n2,z);
xlabel('Time');
ylabel('Amplitude');
title('Convolution with function');
grid on;

```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/c47db7bc-90a0-46ee-9ad7-c3f94341bb2c" height="400px" width="600px"/>
</p>




**3.4.2. Cross correlation of Signal :** 

**Input :**

```matlab
%% cross correlation signal with tebulated method & function

clc
clear all;
close all;

a=0:1:4;
x=[1 2 3 1 2];
y=[1 -1 1 1 -1];
y1= flip(y);

cross_corr=xcorr(x,y);

la=length(x);

lb=length(y1);
ind=la+lb-1;

con_sig=zeros(1,ind);
b=0:length(con_sig)-1;

for i=1:ind
    for j=1:lb
        if (i-j+1)>0 && (i-j+1) <=la
            con_sig(i)=con_sig(i)+y1(j)*x(i-j+1);
        end
    end
end

figure
subplot(4,1,1)
stem(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Signal-01');

subplot(4,1,2)
stem(a,y1);
xlabel('Time');
ylabel('Amplitude');
title('Signal-02');

disp(con_sig)
subplot(4,1,3)
stem(con_sig);
xlabel('Time');
ylabel('Amplitude');
title(' Cross corelation with tabular format');

subplot(4,1,4);
stem(cross_corr);
xlabel('Time');
ylabel('Amplitude');
title('Cross corelation with function');
```

**Output :**

<p align="center">
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/9a2da5e4-42aa-4483-9c5b-e6db42684f93" height="400px" width="600px"/>
</p>





**3.5. Discussion :**

<p align="center">
  
 Here for convolution process we use the default function.
  
 ```matlab
  conv();

```
 In tabular format by using above method we can get the same signal as the using signal of function. Here the number of values in new array is :
 
 summation the number of values in two arrays -1;

 We get the same signal in  two different format.


 For cross correlation process we use the default function.
  
 ```matlab
  xcorr();

```
 In tabular format by using above method we can get the same signal as the using signal of function. At first we flip the any array :

 ```matlab

y=[1 -1 1 1 -1];
y1= flip(y);


```
 
 
 And then following the same process as the covulation by using the inverse signal. We get the same signal in  two different format.

</p>
 
