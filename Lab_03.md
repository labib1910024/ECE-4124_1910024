**3.1. Experiment No. :** 03

**2.2. Experiment Name :** Forming time shifting,auto-correlation and cross-correlation of different types of signal using MATLAB.

**2.3. Theory :**

<p align="center">
  
Time shifting :



</p>


**2.4. MATLAB Signal representation :**

**2.4.1. Advancing of Signal :**

**Input :**

```matlab
%% convulated signal with tebulated method & function

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
title('Convulation with tabular format');
grid on;

subplot(4,1,4);
stem(n2,z);
xlabel('Time');
ylabel('Amplitude');
title('Convulation with function');
grid on;

```

**Output :**

<p align="center">
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/c47db7bc-90a0-46ee-9ad7-c3f94341bb2c">
</p>




**2.4.2. Delaying of Signal :** 

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
 
  <img src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/9a2da5e4-42aa-4483-9c5b-e6db42684f93">
</p>





**2.5. Discussion :**

<p align="center">

 

</p>
 
