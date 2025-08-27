# estimation-of-breathing-and-heart-rate
# Estimation of Breathing Rate and Heart Rate from PPG

This repository contains the work I completed during my **Taiwan Experience Education Program (TEEP) Internship (Summer 2025)** under the guidance of **Prof. Shang-Ping Ying**.  
The project focuses on building an **Arduino-based biosensing system** to acquire **Photoplethysmogram (PPG) signals** and applying **signal processing techniques** for the estimation of **heart rate (HR)** and **breathing rate (BR)**.

---

##  Motivation
Monitoring vital signs such as heart rate and respiration rate is crucial in healthcare, fitness, and early diagnosis of cardiovascular or respiratory disorders. Traditional systems can be costly and bulky, but **PPG sensors** provide a **low-cost, non-invasive, and portable** alternative.  

The goal of this project was to design a compact system capable of:  
- Capturing reliable PPG signals using simple hardware.  
- Processing the signals to estimate HR and BR with good accuracy.  

---

##  System Overview
### Hardware
- **PPG Sensor:** Red LED + photodiode for optical sensing.  
- **Arduino Uno:** Used for signal acquisition and serial data transfer.  
- **Finger Placement Method:** Sensor records variations in light absorption due to blood volume changes in the finger.  

### Software & Tools
- **Arduino IDE** → For microcontroller programming.  
- **Python** → Filtering, peak detection, frequency analysis.  
- **MATLAB** → Validation of algorithms and visualization.  

---

##  Methodology
1. **Signal Acquisition**
   - Raw PPG signals captured using Arduino and sensor module.  
   - Data transferred via serial communication and saved for analysis.  

2. **Preprocessing**
   - Band-pass filter applied (0.5–5 Hz) to remove motion artifacts and noise.  
   - Baseline drift corrected and signal normalized.  

3. **Heart Rate Estimation**
   - Peaks detected in the filtered PPG waveform.  
   - Inter-beat interval (IBI) calculated → converted to BPM.  

4. **Breathing Rate Estimation**
   - Respiratory-induced variations in PPG amplitude and baseline extracted.  
   - FFT performed to determine dominant frequency in the respiratory band (0.1–0.5 Hz).  

---

##  Results
- **Heart Rate:** Estimated within ±2 BPM of reference values.  
- **Breathing Rate:** Validated with controlled breathing cycles.  
- Demonstrated that **low-cost, Arduino-based hardware** can achieve reliable results for basic physiological monitoring.  

---


