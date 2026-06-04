# Mean-Variance-And-Cross-Correlation:

## Aim: 

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed:

• Computer with i3 Processor
• SCI LAB

## Algorithm:

Define the Function:
Specify the function you want to simulate.
For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
Generate Sample Points:
Decide on the range and the number of sample points.
Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation:
Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results:
Output the computed mean variance and Cross Correlation PROCEDURE 
• Refer Algorithms and write code for the experiment. 
• Open SCILAB in System • 
Type your code in New Editor:
• Save the file
• Execute the code 
• If any Error, correct it in code and execute again 
• Verify the generated results.

## Code:
```
clear; 
clc; 
clear;
function X=f(x)
z=4*(1-x)^2,
X=x*z
endfunction 
a=0;
b=1;
EX=intg(a,b,f); 
function y=c(y)
z=4*(1-y)^2,
y=y*z
endfunction 
EY=intg(a,b,c);
disp(EX,"i)Mean of X =")
disp(EY," Mean of Y =")
function X=g(x),
z=3*(1-x)^2,
X=x^2*z
endfunction 
a=0;
b=1;
EX2=intg(a,b,g); 
function Y=h(y)
z=4*(1-y)^2,
Y=y^2*z
endfunction 
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;
disp(vX2,"ii)Variance of X"); 
disp(vY2," Variance of Y");
x= input("type in the reference sequence=");
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);

```
## Output:

<img width="760" height="691" alt="Screenshot 2026-05-21 135454" src="https://github.com/user-attachments/assets/0d308867-9120-4bfd-874d-0f35a4fd955b" />


## Calculation:


i) Mean of X = 0.25 ;Mean of Y = 0.25

ii) Variance of X =0.0375; Variance of Y =0.0375

Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]

## Result:

Thus the mean , variance and cross correlation are executed in Scilab and output is verified
