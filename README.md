# Video Analysis - Motion Detection & Segmentation

A comprehensive implementation of video analysis techniques using OpenCV-Python for detecting and tracking moving objects through spatial and temporal segmentation methods.

## Overview

This project implements various motion detection algorithms on video sequences, comparing their effectiveness in tracking moving objects. The implementation covers basic frame differencing to advanced background subtraction models (MOG2, KNN).

**Video Specifications:** 854×480px @ 24 FPS | 136 frames | ~5.67s duration

## Quick Start

```bash
# Install dependencies
pip install opencv-python numpy

# Run the main script
python video_analysis.py
```

## Repository Structure

```
.
├── video_analysis.py          # Main implementation
├── frames/                    # Extracted frames (generated)
├── results/                   # Segmentation outputs (generated)
└── README.md
```

## Features

- **Video I/O Operations**: Load, extract, and save video frames
- **Spatial Segmentation**: Grayscale conversion, heuristic thresholding, Otsu's method
- **Temporal Segmentation**: 
  - Frame differencing (t-1)
  - Three-frame differencing
  - Adaptive background subtraction
  - MOG2 and KNN background models

## Methods Implemented

### Basic Methods
- **Frame Difference (t-1)**: Simple but prone to ghosting
- **3-Frame Differencing**: N=45 for optimal noise reduction
- **Adaptive Background**: α=0.01 for slow-moving objects

### Advanced Methods (OpenCV)
- **MOG2**: Multi-modal Gaussian mixture with shadow detection
- **KNN**: K-Nearest Neighbors for precise edge detection

## Requirements

- Python 3.x
- OpenCV (cv2)
- NumPy

## Academic Context

**Course:** RT5/2 - Video Analysis Lab  
**Institution:** INSAT, University of Carthage  
**Authors:** Ben Mefteh Shams, Jarboui Nada  
**Academic Year:** 2025/2026

## License

Academic project for educational purposes.

---

*Implementation of motion detection algorithms for video segmentation*