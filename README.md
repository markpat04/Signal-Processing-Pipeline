<div align="center">

# 📡 SignalScope: DSP & Visualization Engine

**A Signal Processing Pipeline**

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific_Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Maintenance-Active-blueviolet)

[View Demo](#-visual-output) • [Installation](#-installation) • [Theory](#-theoretical-background) • [Contribute](#-contributing)

</div>

---

## 📖 Overview

**SignalScope** is a comprehensive educational tool designed to bridge the gap between theoretical Signal Processing and practical Python implementation.

In Data Science, real-world data is rarely clean. It contains noise, outliers, and artifacts. This project simulates that reality by generating perfect waveforms, corrupting them with Gaussian noise, and then using statistical filtering (Moving Average) and Frequency Domain Analysis (FFT) to recover the signal.

### 🎯 Use Cases
* **IoT Sensor Analysis:** Cleaning noisy vibration data from machinery.
* **Financial Modeling:** Smoothing volatile stock market trends.
* **Audio Engineering:** Understanding Signal-to-Noise Ratio (SNR).

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

---

## 🛠️ Installation

### 1. Clone the repository
```bash
git clone [https://github.com/yourusername/SignalScope.git](https://github.com/yourusername/SignalScope.git)
cd SignalScope
