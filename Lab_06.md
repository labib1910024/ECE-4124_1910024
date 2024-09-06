
**6.1. Experiment No. :** 06

**6.2. Experiment Name :**  Z- transform ,poles and zeros by using MATLAB.

**6.3. Theory :**

<p text-align="justify">
  
Z- Transform : 
In mathematics and signal processing, the Z-transform converts a discrete-time signal, which is a sequence of real or complex numbers, into a complex valued frequency-domain (the z-domain or z-plane) representation. It can be considered a discrete-time equivalent of the Laplace transform. The formula is X(z) = Σ x|n|z⁻ⁿ.

Poles and Zeros :
The values of z for which H(z) = 0 are called the zeros of H(z), and the values of z for which H(z) has value are referred to as the poles of H(z). In other words, the zeros are the roots of the numerator polynomial and the poles of H(z) for finite values of z are the roots of the denominator polynomial.

</p>



**6.4. MATLAB Z-Transform representation :**

**6.4.1. Z-Transform  and Inverse transform of a Signal :**

**Input :**

```matlab
clc;
clear all;
close all;

 
x = [1, 2, 5, 6, 7]; 
n = 0:4;           
syms z ;      
X_z = 0;

for i = 1:length(x) 
    X_z = X_z + x(i) * z^(-n(i)); 
end 

X_z = simplify(X_z); 
disp('Z-transform of x[n]:'); 
disp(X_z); 


x_n = iztrans(X_z, z, n); 
disp('Inverse Z-transform:'); 
disp(x_n);

```

**Output :**

<p align="center">

 
 <img  width="254px" alt="image" src="https://github.com/user-attachments/assets/ccf7970c-7a26-47ff-a61c-1c0d852eb1aa">


</p>



**6.4.2. Z-Transform of a Signal at any index position :** 

**Input :**

```matlab
clc;
clear all;
close all;


x = input('Enter the sequence: ');

z_i = input('Enter the starting index: ');


z_index = z_i + 1;

syms z

x_z = 0;
N = length(x);

for i = 1:N
    x_z = x_z + x(i) * z^(-(i - z_index));
end


disp('Z-transform:');
disp(vpa(x_z, 5));
```

**Output :**

<p align="center">
  <img width="253" alt="image" src="github.com/user-attachments/assets/287fd9f8-89a9-4331-aa61-05c7999fa210">
 

</p>



**6.4.3. Poles and Zeros of Z-Transform :** 

**Input :**

```matlab


```

**Output :**

<p align="center">
 
  
  <img width="269" alt="image" src="https://github.com/labib1910024/ECE-4124_1910024/assets/87533597/7ff58110-3da1-4ef7-8bdf-aed459f8e222">

 
</p>


**6.5. Discussion :**

<p text-align="justify">

 Here we use the following formula to determine the z-transform of the signal and vpa(x_z,5) converts the result of the Z-transform to a numeric form with 5 significant digits. After that the code is user define to find out the index and the zeroth position ,and then find out the poles and zeros by the allowed formula


</p>
 


