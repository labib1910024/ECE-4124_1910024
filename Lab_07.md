
**6.1. Experiment No. :** 06

**6.2. Experiment Name :**  Z- transform ,inverse transform , poles and zeros by using MATLAB.

**6.3. Theory :**

<p text-align="justify">
  

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


**6.5. Discussion :**

<p text-align="justify">


 

</p>
 



