
**5.1. Experiment No. :** 05

**5.2. Experiment Name :** Graphical representation of Z- transform ,poles and zeros by using MATLAB.

**5.3. Theory :**

<p text-align="justify">
  
Z- Transform : 
In mathematics and signal processing, the Z-transform converts a discrete-time signal, which is a sequence of real or complex numbers, into a complex valued frequency-domain (the z-domain or z-plane) representation. It can be considered a discrete-time equivalent of the Laplace transform. The formula is X(z) = Σ x|n|z⁻ⁿ.

Poles and Zeros :
The values of z for which H(z) = 0 are called the zeros of H(z), and the values of z for which H(z) has value are referred to as the poles of H(z). In other words, the zeros are the roots of the numerator polynomial and the poles of H(z) for finite values of z are the roots of the denominator polynomial.

</p>



**5.4. MATLAB Z-Transform representation :**

**5.4.1. Z-Transform of a Signal :**

**Input :**

```matlab
clc;
clear all;
close all;
x = [1,2,5,7,0,1];
syms z
n= 0:length(x)-1;
x_z = sum(x .* z.^(-n));
disp(vpa(x_z,5));

```

**Output :**

<p align="center">

 <img src="" height="400px" width="600px"/>

</p>



**5.4.2. Z-Transform of a Signal at any index position :** 

**Input :**

```matlab
clc;
clear all;
close all;
x = [1,2,5,7,0,1];
z_i = input('Enter :');
z_index = z_i + 1;
syms z
x_z = 0;
N = length(x);

for i= 1:N
    x_z = x_z + x(i) *z^(-(i-z_index));
end
 
disp(vpa(x_z,5));

```

**Output :**

<p align="center">
 
  <img src="" height="400px" width="600px"/>

</p>



**5.4.3. Poles and Zeros of Z-Transform :** 

**Input :**

```matlab
clc;
clear all;
close all;

% Data
x = [1, 2, 5, 7, 0, 1];


z_i = input('Enter :');
z_index = z_i + 1;


syms z
x_z = 0;
N = length(x);


for i = 1:N
    x_z = x_z + x(i) * z^(-(i - z_index));
end

disp('Z-transform:');
disp(vpa(x_z, 5));


[num, den] = numden(x_z); % Get numerator and denominator
zeros = solve(num == 0, z); % Find zeros by solving num == 0
poles = solve(den == 0, z); % Find poles by solving den == 0

disp('Zeros:');
disp(vpa(zeros, 5));

disp('Poles:');
disp(vpa(poles, 5));


```

**Output :**

<p align="center">
 
  <img src="" height="400px" width="600px"/>
 
</p>


**5.5. Discussion :**

<p text-align="justify">
  


</p>
 

