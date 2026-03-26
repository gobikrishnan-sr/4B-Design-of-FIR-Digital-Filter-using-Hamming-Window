# FIR-FILTER-DESIGN
# EXP 4 b:

Design-of-FIR-Digital-Filter-using-Hamming-Window

# AIM 1: 

To perform Design-of-LOWPASS FIR-Digital-Filter-using-Hamming-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) = Wc/ %pi ; 
else 
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Hamming Window 
for n = 1:M 
W(n) = 0.54-(0.46*cos((2*%pi*(n-1))/(M-1))); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR LPF using Hamming Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR LPF using Hamming Window'); 
```
# CALCULATION:
<img width="1600" height="919" alt="image" src="https://github.com/user-attachments/assets/18486ba9-ecc2-4af9-ab09-e531ec55602d" />
<img width="1600" height="442" alt="image" src="https://github.com/user-attachments/assets/ea76457a-ec8c-49f8-a9cf-bff5f95f3f69" />


# OUTPUT:
<img width="480" height="425" alt="LPF-Hamming calculation" src="https://github.com/user-attachments/assets/98650c72-45f7-4a39-960a-d5c0ba7a893f" />
<img width="762" height="723" alt="LPF-Hamming Graph" src="https://github.com/user-attachments/assets/ea4e8e5f-500c-4665-ade3-6b6d68ec1d38" />

# RESULT: 

Thus design of low pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
``` 
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =1-Wc/ %pi ; 
else 
hd(n) =-sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Hamming Window 
for n = 1:M 
W(n) = 0.54-(0.46*cos((2*%pi*(n-1))/(M-1))); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR HPF using Hamming Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR HPF using Hamming Window'); 
```
# CALCULATION:
<img width="1600" height="911" alt="image" src="https://github.com/user-attachments/assets/aacc1b74-a618-491b-9db5-e12d6b5b0818" />

<img width="1600" height="417" alt="image" src="https://github.com/user-attachments/assets/0d53a2b7-805b-4829-be73-6b270c022baa" />

# OUTPUT:
<img width="449" height="474" alt="HPF-Hamming Calculation" src="https://github.com/user-attachments/assets/c8aaa300-00c1-4223-8f7a-4102951dcdc3" />
<img width="769" height="727" alt="HPF-Hamming Graph" src="https://github.com/user-attachments/assets/492cc749-dc3e-4a05-9cc1-5ee1d740cd7b" />

# RESULT: 
Thus design of HIGH pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =(Wc2-Wc1)/%pi ; 
else 
hd(n) =((sin(Wc2 *((n -1)-alpha)))-(sin(Wc1 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Hamming Window 
for n = 1:M 
W(n) = 0.54-(0.46*cos((2*%pi*(n-1))/(M-1))); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR BPF using Hamming Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BPF using Hamming Window'); 
```
# CALCULATION:
<img width="1600" height="839" alt="image" src="https://github.com/user-attachments/assets/d0ba16c1-fbd4-45cf-8fb7-22cc37430b2c" />
<img width="1600" height="497" alt="image" src="https://github.com/user-attachments/assets/094f7712-8cf6-4aa5-8410-1ad21c512f3d" />


# OUTPUT:
<img width="570" height="466" alt="BPF-Hamming Calculation" src="https://github.com/user-attachments/assets/c98ab435-43d0-4825-8184-dceec936c362" />
<img width="761" height="724" alt="BPF-Hamming Graph" src="https://github.com/user-attachments/assets/a8a59b4a-8d98-4c2b-92c7-01ad72acc695" />

# RESULT: 
Thus design of BAND pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =1-((Wc2-Wc1)/%pi) ; 
else 
hd(n) =((sin(Wc1 *((n -1)-alpha)))-(sin(Wc2 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Hamming Window 
for n = 1:M 
W(n) = 0.54-(0.46*cos((2*%pi*(n-1))/(M-1))); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR BSF using Hamming Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BSF using Hamming Window'); 
```
# CALCULATION:
<img width="1600" height="1210" alt="image" src="https://github.com/user-attachments/assets/9c5531c8-a9d4-40a3-8456-e51301b31fe7" />

# OUTPUT:
<img width="548" height="507" alt="BSF-Hamming Calculation" src="https://github.com/user-attachments/assets/938874ae-19cb-4b52-93ed-34d5f8b3ea92" />
<img width="758" height="719" alt="BSF-Hamming Graph" src="https://github.com/user-attachments/assets/0d4ba0c2-e435-4271-99d4-6d42aa2adce3" />

# RESULT: 
Thus design of BAND STOP FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.
