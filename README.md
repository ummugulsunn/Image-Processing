# Image Processing - CSE445 Course Assignments

A collection of image processing assignments developed for the **CSE445 - Image Processing** course. The projects cover fundamental to advanced topics including spatial domain operations, histogram enhancement, frequency domain filtering, and optical character recognition (OCR).

---

## Table of Contents

- [Overview](#overview)
- [Assignments](#assignments)
  - [HW1 - Basic Image Operations & Analysis](#hw1---basic-image-operations--analysis)
  - [HW2 - Histogram Enhancement](#hw2---histogram-enhancement)
  - [HW3 - Frequency Domain Filtering](#hw3---frequency-domain-filtering)
  - [Project - Automatic Character Recognition (OCR)](#project---automatic-character-recognition-ocr)
- [Technologies & Libraries](#technologies--libraries)
- [Installation & Setup](#installation--setup)
- [Project Structure](#project-structure)
- [Topics Covered](#topics-covered)
- [Author](#author)

---

## Overview

This repository contains four Jupyter Notebook-based assignments that progressively explore core image processing concepts:

| # | Assignment | Domain | Key Concepts |
|---|-----------|--------|-------------|
| 1 | Basic Image Operations | Spatial | RGB channels, cropping, histograms, colormaps |
| 2 | Histogram Enhancement | Spatial | Equalization, CLAHE, piecewise linear transform |
| 3 | Frequency Domain Filtering | Frequency | FFT, high/low-pass filters, band-stop, PSNR |
| 4 | Automatic Character Recognition | Applied | PDF-to-text OCR, preprocessing, thresholding |

All notebooks are designed to run on **Google Colab** and include inline visualizations and comparisons.

---

## Assignments

### HW1 - Basic Image Operations & Analysis

> **Notebook:** `hw1.ipynb`

Covers fundamental image manipulation techniques:

- **Image Loading & Display** — Reading images with OpenCV and rendering with Matplotlib
- **Cropping** — Extracting 24×24 pixel regions of interest
- **Color Channel Separation** — Isolating and visualizing individual R, G, B channels
- **Pixel Value Inspection** — Accessing and analyzing raw pixel data
- **Colormap Visualization** — Applying viridis, plasma, and inferno colormaps
- **Low-Light Image Analysis** — Investigating underexposed images and their histograms
- **Histogram Generation** — Computing and plotting intensity distributions

---

### HW2 - Histogram Enhancement

> **Notebook:** `HW2_HistogramEnhancement.ipynb`

Implements contrast enhancement techniques using an object-oriented architecture:

- **Histogram Equalization** — Global contrast enhancement via CDF mapping
- **CLAHE** (Contrast Limited Adaptive Histogram Equalization) — Localized adaptive enhancement to avoid over-amplification
- **Piecewise Linear Transform** — Custom intensity mapping with breakpoints
- **Cumulative Histogram Visualization** — CDF plots for before/after comparison

**Architecture:**
| Class | Responsibility |
|-------|---------------|
| `ImageProcessor` | Image loading, histogram computation |
| `EnhancementMethods` | Equalization, CLAHE, piecewise linear transform |
| `VisualReporter` | Side-by-side comparison visualizations |

---

### HW3 - Frequency Domain Filtering

> **Notebook:** `HW3_ different_filtering_operations_on_the_image_in_the_frequency domain.ipynb`

Explores image filtering in the frequency domain using 2D Fourier Transform:

- **Synthetic Image Generation** — Creating geometric shapes for controlled experiments
- **2D FFT & Spectrum Analysis** — Transforming images to frequency domain and visualizing magnitude spectrum
- **High-Pass Filtering** — Edge detection by preserving high-frequency components
- **Low-Pass Filtering** — Smoothing by attenuating high-frequency components
- **Periodic Noise Injection** — Adding cosine-based noise patterns
- **Band-Stop Filtering** — Selective frequency removal for noise elimination
- **PSNR Calculation** — Quantitative quality assessment of filtered results

**Key Functions:**
```
high_pass_filter(image, cutoff)    — Removes low-frequency components
low_pass_filter(image, cutoff)     — Removes high-frequency components
band_stop_filter(image, freq, bw)  — Removes a specific frequency band
psnr(original, filtered)           — Computes Peak Signal-to-Noise Ratio
```

---

### Project - Automatic Character Recognition (OCR)

> **Notebook:** `AUTOMATIC CHARACTER RECOGNITION.ipynb`

A practical application that converts PDF documents to structured Excel files using OCR:

- **PDF to Image Conversion** — Rendering PDF pages as high-resolution images
- **Image Preprocessing Pipeline:**
  - Grayscale conversion
  - Adaptive thresholding (Gaussian)
  - Non-local means denoising
- **OCR with Tesseract** — Text extraction supporting English and Turkish
- **Text Post-Processing** — Cleaning illegal characters and structuring output
- **Excel Export** — Organized tabular output via Pandas
- **Accuracy Evaluation** — Comparing OCR results against manual transcription

---

## Technologies & Libraries

| Library | Purpose |
|---------|---------|
| **OpenCV** (`cv2`) | Core image processing operations |
| **NumPy** | Numerical computations and array manipulation |
| **Matplotlib** | Visualization and plotting |
| **SciPy** | FFT, frequency domain operations |
| **Tesseract** (`pytesseract`) | Optical character recognition engine |
| **pdf2image** | PDF page rendering |
| **Pandas** | Data structuring and Excel export |

---

## Installation & Setup

### Option 1: Google Colab (Recommended)

All notebooks are designed for Google Colab. Simply upload the notebook and run — dependencies are installed inline via `!pip install` commands.

### Option 2: Local Environment

```bash
# Clone the repository
git clone https://github.com/ummugulsunn/Image-Processing.git
cd Image-Processing

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # macOS/Linux
# venv\Scripts\activate   # Windows

# Install dependencies
pip install numpy matplotlib opencv-python scipy pytesseract pdf2image pandas

# For Tesseract OCR engine (required for the OCR notebook)
# macOS
brew install tesseract

# Ubuntu/Debian
# sudo apt install tesseract-ocr tesseract-ocr-tur

# Launch Jupyter
jupyter notebook
```

---

## Project Structure

```
Image-Processing/
│
├── hw1.ipynb                          # HW1: Basic image operations & analysis
├── HW2_HistogramEnhancement.ipynb     # HW2: Histogram enhancement techniques
├── HW3_ different_filtering_...ipynb  # HW3: Frequency domain filtering
├── AUTOMATIC CHARACTER RECOGNITION.ipynb  # OCR project
└── README.md
```

---

## Topics Covered

```
Image Processing
├── Spatial Domain
│   ├── Pixel-level operations
│   ├── Color channel manipulation
│   ├── Histogram analysis
│   ├── Histogram equalization
│   ├── CLAHE
│   └── Piecewise linear transform
│
├── Frequency Domain
│   ├── 2D Fourier Transform (FFT)
│   ├── Frequency spectrum visualization
│   ├── High-pass filtering
│   ├── Low-pass filtering
│   ├── Band-stop filtering
│   └── PSNR quality metric
│
└── Applied
    ├── Image preprocessing for OCR
    ├── Adaptive thresholding
    ├── Non-local means denoising
    └── Tesseract OCR integration
```

---

## Author

**Ümmügülsün Türkmen**

- GitHub: [@ummugulsunn](https://github.com/ummugulsunn)

---

<p align="center">
  <i>CSE445 - Image Processing | Group 9</i>
</p>
