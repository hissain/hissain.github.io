---
layout: post
title: "Introducing jSciPy: Scientific Computing for Java"
date: 2025-12-31 12:00:00 +0600
thumbnail: ""
description: In modern machine learning workflows, most signal processing tasks rely on Python's SciPy utilities. However, there is no Java library that replicates SciPy's behavior with comparable completeness and consistency. This creates a significant gap for teams building ML or signal processing pipelines on the JVM. jSciPy aims to fill this gap, and the demand for such a library is higher than ever.
tags:
  - Java
  - Open Source
  - Scientific Computing
  - Signal Processing
  - Android
author: Sazzad Hissain Khan
---
![](/assets/images/uploads/signal-processing18-banner.jpg)

If you come from a Python background, you undoubtedly know [SciPy](https://scipy.org/) — the fundamental library for scientific computing. But what if you are building an Android app or a high-performance backend service on the JVM?

**jSciPy** is my attempt to fill that gap. It is a Java Scientific Computing Library designed for **Signal Processing**, **Machine Learning**, and **Data Science workflows**, providing a familiar API for developers used to NumPy and SciPy.

## Key Features

### 1. Advanced Filtering

Implemented from scratch to match SciPy's output:

It currently includes modules for:
*   **Signal Processing**: Butterworth filters, Savitzky-Golay smoothing, Peak detection.
*   **Transformations**: FFT (Fast Fourier Transform), Hilbert Transform, Convolution.
*   **Math & Analysis**: RK4 ODE Solver, Interpolation (Linear, Cubic Spline), Resampling.

### 2. Signal Analysis

* **Peak Detection**: Find peaks in noisy signals with height, distance, and prominence filters (similar to `scipy.signal.find_peaks`).
* **Spectral Analysis**: Welch's Method for Power Spectral Density (PSD).
* **Fast Fourier Transforms**: Efficient FFT and RFFT wrappers.

### 3. Math & Solvers

* **RK4 Solver**: Runge-Kutta 4th Order method for solving ordinary differential equations (ODEs).
* **Interpolation**: Linear and Cubic Spline interpolation.
* **Smoothing**: Savitzky-Golay filters for smoothing noisy data while preserving peak heights.

## Example Usage

Here is how you can apply a low-pass filter to a signal, just like in Python:

```java
import com.hissain.jscipy.signal.Signal;

double[] data = { ... }; // Your noisy signal
double sampleRate = 100.0;
double cutoff = 10.0;
int order = 4;

// Apply zero-phase low-pass filter
double[] cleanData = Signal.filtfilt(data, sampleRate, cutoff, order);
```

## Get Started

jSciPy is open source and available on GitHub. You can include it in your project via JitPack.

[View on GitHub](https://github.com/hissain/jSciPy)
