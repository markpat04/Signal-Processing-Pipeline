<div align="center">

# 📡 A Signal Processing Pipeline


![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific_Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Maintenance-Active-blueviolet)

[View Demo](#-visual-output) • [Theory](#-theoretical-background)

</div>

---

## 📖 Overview

This project demonstrates an end-to-end workflow for **Digital Signal Processing (DSP)** in Python. It simulates real-world signal data challenges by generating synthetic waveforms, introducing Gaussian noise, and applying statistical filtering techniques to recover the original signal.

The project is designed to visualize the difference between **Time Domain** (how signals look) and **Frequency Domain** (what signals are composed of) using Fast Fourier Transforms (FFT).

---

## ⚡ Key Features

* **🌊 Multi-Wave Generation:** Create Sine, Square, and Sawtooth waveforms programmatically.
* **📉 Noise Injection Engine:** Configurable Gaussian noise generator to test algorithm robustness.
* **🧹 Digital Filtering:** Implementation of convolution-based Moving Average filters.
* **📊 Dual-Domain Visualization:**
    * **Time Domain:** Amplitude vs. Time.
    * **Frequency Domain:** Magnitude vs. Frequency (FFT).
* **🧮 Statistical Profiling:** Automatic calculation of Mean, RMS, and SNR (dB).

---

## 📸 Visual Output

The script outputs a high-resolution, publication-ready 4x3 dashboard:

| Row | Analysis Layer | Description |
| :--- | :--- | :--- |
| **1** | **Ground Truth** | The perfect, mathematically generated signals. |
| **2** | **Noisy Input** | Signals corrupted by random factors (simulating real sensors). |
| **3** | **Filtered Output** | The result of the noise-reduction algorithms. |
| **4** | **Spectral Analysis** | Fast Fourier Transform (FFT) comparing frequency components. |

> *Note: Run the script to generate the interactive Matplotlib window.*

---

## 📐 Theoretical Background

This project applies core mathematical concepts to code.

### 1. Signal-to-Noise Ratio (SNR)
We quantify signal quality using SNR in decibels (dB). A higher dB indicates a cleaner signal.

$$SNR_{dB} = 10 \log_{10}\left(\frac{P_{signal}}{P_{noise}}\right)$$

### 2. Moving Average Filter (Convolution)
We smooth the data by convolving the signal with a normalized window vector.

$$y[n] = \frac{1}{M} \sum_{j=0}^{M-1} x[n-j]$$

Where $M$ is the window size (`filter_window` in the config).

<img width="1613" height="895" alt="Screenshot 2025-12-24 163613" src="https://github.com/user-attachments/assets/bc311e2b-2f93-4cc8-a31e-66e7b2dc7c82" />
