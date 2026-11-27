# gloria-mbilinyi-COU07506-labs
# COU 07506 — Digital Signal Processing Laboratory

**Dar es Salaam Institute of Technology (DIT)**  
**Department of Computer Studies**  
**Academic Year:** 2026/2027 | Semester I

## Student Information

| Field | Details |
|---|---|
| Student Name | Gloria Beneth Mbilinyi |
| Registration Number | 240242493088 |
| Group | 08 |
| Programme | Bachelor of Engineering in Computer Engineering |
| Module | COU 07506 — Digital Signal Processing |
| Laboratory Platform | Google Colab |
| Completed Labs | Weeks 1–5 |

## Project Overview

This repository contains the Python implementations, experimental results, visualizations, and analysis completed for the Digital Signal Processing laboratory course at the Dar es Salaam Institute of Technology.

The laboratory activities cover discrete-time signals, sampling and quantization, convolution and correlation, z-transforms, system stability, and Fast Fourier Transform (FFT) algorithms.

Each week's notebook includes Python code, numerical results, graphs, observations, and theoretical analysis based on the official laboratory manual.

## Laboratory Activities

### Week 1 — Lab 0: Setting Up the DSP Laboratory

**Focus:** Introduction to Python-based Digital Signal Processing.

Activities completed:
- Generated elementary discrete-time signals, including unit impulse, step, ramp and exponential sequences.
- Investigated signal parameters and visualized discrete-time signals.
- Imported and processed a recorded voice signal.
- Converted an M4A recording into WAV format.
- Normalized, plotted and played a five-second audio recording.
- Used NumPy, SciPy, Matplotlib and Google Colab.

**Results:** Successfully analyzed a voice recording sampled at 44,100 Hz and plotted its waveform.

### Week 2 — Lab 1A: Sampling, Aliasing and Quantization

**Focus:** Sampling theory, aliasing, anti-aliasing filters and quantization.

Activities completed:
- Simulated aliasing at different sampling rates.
- Compared audio downsampling with and without anti-aliasing filtering.
- Implemented uniform quantization.
- Verified the approximately 6 dB-per-bit rule.
- Quantized a recorded voice at different bit depths.

**Experimental Results:**

| Quantization Bits | Measured SQNR |
|---|---|
| 4 bits | 16.35 dB |
| 8 bits | 40.27 dB |
| 12 bits | 64.36 dB |

**Observation:** Increasing the quantization bit depth improved SQNR and reduced quantization noise. Anti-aliasing filtering also improved perceived audio clarity during downsampling.

### Week 3 — Lab 1B: Convolution, Correlation and Difference Equations

**Focus:** Discrete-time systems, convolution, correlation and system responses.

Activities completed:
- Implemented linear convolution manually and verified it with NumPy.
- Applied moving-average filters to noisy signals.
- Tested system linearity and time invariance.
- Estimated signal delay using cross-correlation.
- Solved difference equations using direct recursion and SciPy.

**Experimental Results:**

| Parameter | Result |
|---|---|
| Manual convolution time | 3.795 s |
| NumPy convolution time | 0.0026 s |
| Convolution speed-up | 1,437.84× |
| Best moving-average filter | M = 9 |
| Minimum MSE | 0.0334 |
| Estimated signal delay | 37 samples |
| Final step-response value | 5.3333 |

**Observation:** NumPy convolution was substantially faster than manual Python loops. The moving-average filter reduced noise, and cross-correlation successfully detected the signal delay under moderate noise conditions.

### Week 4 — z-Transform Laboratory: Poles, Zeros and Stability

**Focus:** z-transforms, pole-zero diagrams, impulse responses and digital resonator design.

Activities completed:
- Implemented pole-zero plotting.
- Computed inverse z-transforms using partial-fraction expansion.
- Investigated the relationship between pole locations and system stability.
- Classified the stability of four digital systems.
- Designed a second-order digital resonator.
- Compared original white noise with filtered resonator audio.

**Experimental Results:**

| Parameter | Result |
|---|---|
| Resonator sampling frequency | 8,000 Hz |
| Target resonant frequency | 1,000 Hz |
| Pole radius | 0.97 |
| Measured resonance peak | 1,000.98 Hz |
| Resonator stability | BIBO Stable |

**Observation:** Poles inside the unit circle produced stable causal systems. Increasing the pole radius toward the unit circle produced sharper resonance and longer-lasting oscillations.

### Week 5 — Lab 2: Implementing the FFT

**Focus:** DFT, radix-2 FFT, bit reversal, zero-padding and frequency-domain convolution.

Activities completed:
- Computed the DFT using matrix multiplication.
- Implemented bit-reversal indexing.
- Developed an iterative radix-2 FFT algorithm.
- Compared execution times of direct DFT, custom FFT and NumPy FFT.
- Investigated zero-padding and the DTFT.
- Implemented linear and circular convolution using FFTs.

**FFT Performance Results (N = 4096):**

| Method | Execution Time |
|---|---|
| Direct DFT | 1.562888 s |
| Custom Radix-2 FFT | 0.034776 s |
| NumPy FFT | 0.000201 s |

**Custom FFT Speed-up:** 44.94×

The circular convolution experiment produced the expected result `[3, 2, 3, 2]`.

**Observation:** FFT algorithms reduced computation time compared with direct DFT for large input sizes. Zero-padding increased frequency sampling density without adding information to the original signal.

## Repository Structure

```text
COU07506-labs/
│
├── README.md
│
├── Week01/
│   └── COU07506_Week01_240242493088.ipynb
│
├── Week02/
│   └── COU07506_Week02_240242493088.ipynb
│
├── Week03/
│   └── COU07506_Week03_240242493088.ipynb
│
├── Week04/
│   └── COU07506_Week04_240242493088.ipynb
│
└── Week05/
    └── COU07506_Week05_240242493088.ipynb
```

*The structure above is the intended organization of the repository.*

## Technologies and Tools

- Python 3
- Google Colab
- NumPy
- SciPy
- Matplotlib
- GNU Octave (Week 1)
- Git and GitHub

## How to Run the Laboratory Notebooks

1. Open the relevant `.ipynb` file in Google Colab.
2. Select **Runtime → Run all**.
3. Upload any required audio recordings when prompted.
4. Examine the numerical outputs, signal plots and analysis sections.
5. Compare results with the expected values in the laboratory manual.

## Learning Outcomes

Through these laboratory exercises, I developed practical skills in:

- Digital signal generation and visualization.
- Sampling, aliasing and quantization.
- Convolution, filtering and correlation.
- Analysis of Linear Time-Invariant systems.
- z-transforms and system stability.
- FFT implementation and performance evaluation.
- Signal-processing applications using Python.

## References

1. Dar es Salaam Institute of Technology. (2026). *COU 07506 Digital Signal Processing Laboratory Manual, Academic Year 2026/2027*.
2. NumPy Documentation: https://numpy.org/doc/
3. SciPy Documentation: https://docs.scipy.org/doc/scipy/
4. Matplotlib Documentation: https://matplotlib.org/stable/

## AI-Use Declaration

ChatGPT was used as a learning assistant for understanding laboratory instructions, explaining Python implementations, troubleshooting code and interpreting experimental results.

The laboratory programs were executed in Google Colab, and their outputs were examined and compared with theoretical expectations.

---

**Prepared by:** Gloria Beneth Mbilinyi  
**Programme:** Bachelor of Engineering in Computer Engineering  
**Institution:** Dar es Salaam Institute of Technology  
**Academic Year:** 2026/2027
