# Smart Embedded Pipeline Steam Leakage Detection System
**Edge-Deployed CNN with Temperature Scaling and Safety-First Calibration**

## Overview
This project implements a high-recall visual detection system for high-pressure steam leaks, optimized for the **Raspberry Pi 5**. Unlike standard models that prioritize overall accuracy, this system is calibrated to ensure **Zero False Negatives**, prioritizing industrial safety.

## Tech Stack
* **Hardware:** Raspberry Pi 5 (8GB), Pi Camera Module V2, Active Cooler.
* **Architecture:** EfficientNet-B0 (Quantized to TFLite).
* **Software:** Python 3.10, OpenCV, TensorFlow Lite, RPi.GPIO.

## Key Features
* **Safety-First Thresholding:** Decision threshold tuned to **0.45** to achieve **100% Recall** on test sets.
* **Temperature Scaling ($T=2.0$):** Post-training calibration to fix model overconfidence and produce reliable probability scores.
* **Edge Optimization:** Fully offline inference with a physical hardware interrupt (5V Buzzer/LED) for real-time alerts.

## Results
| Metric | Score |
| :--- | :--- |
| **Recall (Safety Priority)** | **100.00%** |
| **Accuracy** | 90.12% |
| **Precision** | 82.61% |

## Repository Structure
/
├── hardware/        
├── src/               
├── model/             
├── dataset/            
├── documentation/
└── README.md           

## Publication
The full research paper detailing the methodology and hardware integration is available in the `documentation/` folder.
