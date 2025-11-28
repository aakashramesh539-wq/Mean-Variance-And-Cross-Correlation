# Mean-Variance-And-Cross-Correlation:

## Aim: 

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed:

• Computer with i3 Processor • SCI LAB

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
clear; clc; clear;
function X = f(x)
    X = 5 * x .* (3 + x).^2;
end
a = 0;
b = 1;
EX = intg(a, b, f);
function Y = c(y)
    Y = 5 * y .* (3 + y).^2;
end
EY = intg(a, b, c);
mprintf("i)   Mean of X = %.2f\n     Mean of Y = %.2f\n", EX, EY);
function X = g(x)
    X = x.^2 .* 5 .* (3 + x).^2;
end
EX2 = intg(a, b, g);
function Y = h(y)
    Y = y.^2 .* 5 .* (3 + y).^2;
end
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
mprintf("ii)  Variance of X = %.6f\n     Variance of Y = %.6f\n", vX2, vY2);

x= input("type in the reference sequence="); 
y= input("type in the second sequence   =");

n1=max(size(y))-1;
n2=max(size(x))-1;

r=corr(x,y,n1);

clf();
plot2d3(1:length(r), r);
```
## Output:

![WhatsApp Image 2025-11-20 at 17 57 00_ea6ae754](https://github.com/user-attachments/assets/8fc10509-f5ce-4244-b44c-322acf05067b)

## Calculation:

![WhatsApp Image 2025-11-28 at 21 15 44_34b898f4](https://github.com/user-attachments/assets/77a5d6fb-fb4f-4396-ab41-f1f90a52ec27)
![WhatsApp Image 2025-11-28 at 21 15 44_dba36154](https://github.com/user-attachments/assets/fda3e728-8d6a-461e-b231-af7234980436)
![WhatsApp Image 2025-11-28 at 21 16 40_4ff50186](https://github.com/user-attachments/assets/f511df85-8c27-46f1-90a9-8ff59591fe48)


i) Mean of X = 47.25 ;Mean of Y = 47.25

ii) Variance of X =-2199.6625; Variance of Y =-2199.6625

Cross Correlation: Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]

## Result:

Thus the mean , variance and cross correlation are executed in Scilab and output is verified
