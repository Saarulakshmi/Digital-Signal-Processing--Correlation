# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
```
% Saaru Lakshmi D 212223050040
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
% INPUT SIGNAL-1
a=input('enter the starting x(n)');
x=input('Enter the x(n) sequence');
n=a:1:length(x)+a-1;
figure(1)
stem(n,x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')
% INPUT SIGNAL 2
b=input('enter the starting y(n)');
y=input('Enter the y(n) sequence');
m=input('enter the ending y(n)');
n1=b: 1:length(y)+b-1;
figure(2)
stem(n1,y)
xlabel('Time')
ylabel('Amplitude')
title('Input signal-2')
% DISCRETE AUTO CORRELATED SIGNAL
out1=xcorr(x,x)
n2=a-m:1:length(out1)+a-m-1;
figure(3)
stem(n2,out1)
xlabel('Time')
ylabel('Amplitude')
title(' Discrete auto correlated waveform')

% DISCRETE CROSS CORRELATED SIGNAL
Out2=xcorr(x,y);
n3=a-m:1:length(Out2)+a-m-1;
figure(4)
stem(n3,Out2)
xlabel('Time')
ylabel('Amplitude')
title(' Discrete cross correlated waveform')
```

## OUTPUT:
<img width="1600" height="771" alt="image" src="https://github.com/user-attachments/assets/4af6c347-0c14-49af-885b-b310b97a950c" />
<img width="1600" height="805" alt="image" src="https://github.com/user-attachments/assets/30496a5d-f7ad-40d5-9f76-51f338e0b07d" />
<img width="1600" height="788" alt="image" src="https://github.com/user-attachments/assets/61e6cad2-8aa7-4dbd-a798-9340b7aaf721" />
<img width="1600" height="784" alt="image" src="https://github.com/user-attachments/assets/f3e01e03-5e66-4dd0-91f3-28dc492e8879" />

## RESULT:
The cross correlation of x1[n] and x2[n] is {-9,-2.8,10.51,-25.65,1.73,36.19,-11.73,34.85,-14.8,10.5,13.5}
