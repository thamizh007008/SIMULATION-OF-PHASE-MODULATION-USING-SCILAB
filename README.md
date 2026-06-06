# SIMULATION-OF-PHASE-MODULATION-USING-SCILAB
# AIM:

To implement and analyze phase modulation (PM) using SICLAB.

# APPARATUS REQUIRED:

•	Computer with i3 Processor

•	SCI LAB

# THEORY:
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:

<img width="606" height="341" alt="image" src="https://github.com/user-attachments/assets/5832c912-8ddb-4f98-b233-5c092a6442ae" />


# ALGORITHM:

1.	Initialize Parameters:

o	Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).

2.	Generate Time Axis:

o	Create a time vector for the signal duration based on the sampling frequency.

3.	Generate Message Signal:

o	Define the message signal as a cosine wave.

4.	Generate PM Signal:

o	Apply the PM modulation formula to obtain the modulated signal.

5.	Plot the Signals:

o	Use Scilab to plot the message signal, carrier signal, and phase-modulated signal.

# PROGRAM:
```
Am=15.7;
fm=1984;
fs=198400;
t=0:1/fs:2/fm;
Ac=26.69;
fc=19840;
B=5.1;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos((2*3.14*fc*t)+B*sin(2*3.14*fm*t)); 
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos((2*3.14*fc*t)+B*cos(2*3.14*fm*t));
subplot(4,1,4);
plot(t,epm);
```
# OUTPUT:
<img width="1600" height="811" alt="WhatsApp Image 2026-06-06 at 8 22 36 AM" src="https://github.com/user-attachments/assets/3075433d-05a6-4c00-ad44-ca9797a592e9" />

 
# SIGNED OUTPUT:
<img width="1280" height="852" alt="WhatsApp Image 2026-06-06 at 8 23 26 AM" src="https://github.com/user-attachments/assets/6cde46a9-0cac-43a7-9a59-fe460c2ed828" />

# RESULT:

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
