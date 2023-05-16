# Bus-Impedance-Admittance-Matrix
MATLAB Code for matrix calculation of impedance or admittance values for each pair of buses in a Power System.

Here is the code:

clc;
clear all;
close all;
n=input('Enter the number of buses');
fprintf('Enter your choice');
p=input('1.impedance 2. admittance');
if (p==1)
    for q=1:n
        for r= 1:n
            fprintf('Enter the impedance value between %d-%d', q,r);
            z(q,r)=input(':');
            if (z(q,r)==0)
                y(q,r)=0;
            else y(q,r)=inv(z(q,r))
            end
        end
    end
end


This MATLAB code prompts the user to enter the number of buses and their choice of impedance or admittance. Based on the user's choice, it creates a matrix of impedance or admittance values for each pair of buses.

Let's break down the code step by step:

clc;, clear all;, close all;: These are MATLAB commands to clear the command window, workspace variables, and close any open figures, respectively. They ensure a clean workspace before running the code.

n = input('Enter the number of buses');: This line prompts the user to enter the number of buses and assigns the input value to the variable n.

fprintf('Enter your choice');: This line prints the message "Enter your choice" to the command window.

p = input('1.impedance 2. admittance');: This line prompts the user to enter their choice of either impedance or admittance and assigns the input value to the variable p.

if (p==1): This is an if statement that checks if the value of p is equal to 1. If it is, the code proceeds with the impedance calculation.

for q=1:n: This is a for loop that iterates from 1 to the value of n (number of buses). It represents the index of the first bus.

for r=1:n: This is another nested for loop that iterates from 1 to the value of n. It represents the index of the second bus.

fprintf('Enter the impedance value between %d-%d', q, r);: This line prints the message "Enter the impedance value between x-y" to the command window, where x and y are the values of q and r, respectively.

z(q,r) = input(':');: This line prompts the user to enter the impedance value between the q-th and r-th buses and assigns the input value to the matrix element z(q,r).

if (z(q,r)==0): This is an if statement that checks if the impedance value is equal to zero.

y(q,r) = 0;: If the impedance value is zero, it assigns zero to the corresponding element in the matrix y.

else y(q,r) = inv(z(q,r));: If the impedance value is non-zero, it calculates the inverse of the impedance value using the inv() function and assigns it to the corresponding element in the matrix y.

The code provided only covers the case where the user chooses impedance (option 1). It does not include the code for the admittance calculation (option 2).












