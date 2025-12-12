# TIMS Modulation Analysis  
### Analog & Digital Communication Experiments Using TIMS Hardware and PicoScope

## Project Description
This project explores several analog and digital modulation techniques using the **TIMS communications training system** and **PicoScope** for waveform capture. Time-domain and frequency-domain measurements were analyzed to understand modulation behavior, bandwidth requirements, and signal integrity under different channel conditions. Eye diagrams were also generated to evaluate symbol timing, intersymbol interference, and maximum data rate.

The goal of this project is to demonstrate practical communication-system concepts using real hardware and measurement tools.

---

## Modulation Techniques Analyzed

### **Analog Modulation**
| Technique | Time-Domain | Frequency-Domain |
|----------|-------------|------------------|
| **AM** (Amplitude Modulation) | ✔ | ✔ |
| **FM** (Frequency Modulation) | ✔ | ✔ |
| **PM** (Phase Modulation)     | ✔ | ✔ |

### **Digital Modulation**
| Technique | Time-Domain | Frequency-Domain |
|----------|-------------|------------------|
| **ASK** (Amplitude Shift Keying) | ✔ | ✘ |
| **FSK** (Frequency Shift Keying) | ✔ | ✘ |
| **BPSK** (Binary Phase Shift Keying) | ✔ | ✘ |

### **Eye Diagrams**
- 3 different channel environments  
- Observed symbol overlap, ISI, and eye opening  
- Used to estimate maximum data rate for each channel

---

## Experimental Setup

### **Hardware**
- **TIMS Communication System**  
  Used to generate analog/digital modulated carriers.  
- **PicoScope**  
  Captured time and frequency domain signals for analysis.  
- **PC MATLAB / PicoScope Software**  
  Used for visualization and measurement.

### **Signal Chain**
1. TIMS module configured for selected modulation scheme  
2. Output fed into PicoScope  
3. Time-domain waveform captured  
4. FFT mode used (when applicable) for spectrum analysis  
5. Parameters recorded:  
   - carrier frequency  
   - modulation index  
   - bandwidth  
   - symbol rate (digital)  
   - amplitude shaping  

---

## Key Observations

### **Amplitude Modulation (AM)**
- Clear upper and lower sidebands in frequency domain  
- Carrier amplitude remained constant  
- Modulation index affected sideband magnitude

### **Frequency Modulation (FM)**
- Frequency deviation easily visible in time-domain  
- Spectrum spread depending on modulation sensitivity  
- Observed Bessel-type sideband clustering

### **Phase Modulation (PM)**
- Phase discontinuities visible at message transitions  
- Similar bandwidth behavior to FM for equivalent deviation

---

### **Digital Schemes (ASK / FSK / BPSK)**

#### **ASK**
- Amplitude jumps between two levels  
- No frequency-domain plot collected  
- Sensitive to noise (amplitude-based)

#### **FSK**
- Distinct shifts between two frequencies  
- Clean frequency transitions in time-domain  
- Robust to amplitude noise

#### **BPSK**
- Phase flips of 180° clear in time-domain  
- Highest noise immunity of the three  
- No frequency plot collected due to equipment limitations

---

## Eye Diagram Analysis
Three different channel conditions were tested:

- Clean channel  
- Mild ISI channel  
- Severe ISI / bandwidth-limited channel  

Measured eye diagrams showed:

- Eye opening decreases as channel distortion increases  
- Symbol overlap visible under ISI  
- Maximum data rate inferred from horizontal eye width  
- Noise margin inferred from vertical height  

---

## Skills Demonstrated
- TIMS hardware configuration  
- PicoScope operation (time + FFT mode)  
- Modulation/demodulation fundamentals  
- Spectral analysis  
- Eye diagram interpretation  
- Understanding of ISI and channel effects  
- Documentation & communication-system reporting
