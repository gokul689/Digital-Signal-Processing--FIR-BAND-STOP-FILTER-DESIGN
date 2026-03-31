# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc1=input('enter the value of wc1');
wc2=input('enter the value of wc2');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Band Stop Filter Coefficient 
n=0:1:N-1;  
hd=(sin(wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./(pi*(n-alpha+eps)) 
%Bartlett Window Sequence 
n=0:1:N-1; 
wh = 1 - (2*abs(n-alpha))/(N-1)
hn=hd.*wh
% Plot the Low Pass Filter with Hamming Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```
## OUTPUT:

<img width="700" height="624" alt="Screenshot 2026-03-29 082008" src="https://github.com/user-attachments/assets/aa021b6f-65c5-447d-be10-7e40e6b31a21" />

## RESULT:
<img width="1594" height="704" alt="image" src="https://github.com/user-attachments/assets/991cc9a1-482e-4955-a7ed-d7ce99cf77ca" />

