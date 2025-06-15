# Heart Monitor Using IR-Sensor (with ABBA HADIL)
This folder contains a LabVIEW project that implements a heart rate (BPM) monitoring system using IR (infrared) sensors. The project was carried out as part of my academic work at the University of Montpellier.
![Image](https://github.com/user-attachments/assets/f685c43c-f2de-427b-97de-6a332209987c)
## Project Overview
Purpose:
To measure heart rate (BPM) in real time using IR sensors and advanced signal processing techniques implemented in LabVIEW.

## How it Works:
The IR sensor captures a raw analog signal from a fingertip or earlobe. This signal, which contains the heartbeat waveform, is processed in LabVIEW to extract meaningful heart rate data.
![Image](https://cdn10.bigcommerce.com/s-e8bcgbwxqx/products/39898/images/29178/PBDS100A1__02738.1475604299.1280.1280.JPG?c=2)

## Key Features:

-**Signal Acquisition:** Collects real IR data snapshots during lab sessions.
-**Signal Processing:**
  - Noise reduction and filtering to clean up the raw signal.
  - Peak detection algorithms to identify heartbeats.
  - Calculation of BPM from detected peaks.
  - Visualization: Real-time plotting of the signal and detected heartbeats in the LabVIEW front panel.
## Files Included:
  - **BPM Calculator.vi:**
A subVI used to calculate heart rate (BPM) based on detected signal peaks.

  - **Offset Remover.vi:**
Removes the median amplitude value from the signal to enhance peak detection accuracy.

  - **dt.vi:**
Computes the time difference between samples (delta t), useful for time-domain analysis.

  - **Peaks&Valleys_Finder.vi:**
Identifies peaks in the signal. Valley detection has been disabled but can be easily re-enabled if needed.

  - **zero_Padder.vi:**
Performs zero-padding on the signal to improve frequency resolution during Fourier Transform (FFT), allowing for more precise frequency component visualization.

  - **Prj final.vi:**
Project VI

## How to use
1. Clone the repository or just download the Heart Monitor files
```
git clone https://github.com/BekdoucheAmineAdel/LabView-UM.git
cd Twenty-French-Guys-UM
```
2. Open `Prj final. vi`. Make sure to have labview installed (This project is compatible with the version 2024Q3).
3. Adjust the filter parameters
<p align="center">
  <img src="https://github.com/user-attachments/assets/e024c977-edfa-4449-99e7-888605a2441c" alt="Results" width="200" height="200">
</p>
5. Adjust the width on the peaks detector, I chose 50ms as the minimum width between two peaks
<p align="center">
  <img src="https://github.com/user-attachments/assets/6d317027-eaab-4f66-b771-5a10b1ffde7a" alt="Results" width="200" height="150">
</p>
6. Click on the run button in the top pannel

## Results
<p align="center">
  <img src="https://github.com/user-attachments/assets/317b1d04-3b80-4dc3-afa8-4824554a591b" alt="Results" width="600" height="700">
</p>

This screenshot showcases the results. BMP Tone is one methode we used to retrieve the heartrate from the signal acquired and MOY BMP was calculated using the location of the peaks values as you can see both method gives close values around 64 BPM.

## Notes
This project demonstrates the end-to-end process of acquiring, cleaning, and analyzing physiological signals using LabVIEW. All signal processing was performed manually, providing a deeper understanding of the techniques involved in heart rate monitoring.
