# Computer Vision Lab 3 – Feature Detection and Matching  
**Date:** October 3, 2025  
**University:** Luleå University of Technology  
**Course:** Computer Vision  

---

## Overview
This lab introduces students to **feature detection and matching techniques** used in modern computer vision.  
You will implement, evaluate, and compare **corner detectors** and **feature descriptors**, and apply them to **real-world robotic stereo data**.

---

## Learning Outcomes
By completing this lab, you will be able to:

- Implement and evaluate the **Harris Corner Detector**.  
- Apply and compare **SIFT** and **Harris** features for image matching.  
- Analyze **feature matching performance** in stereo video feeds.  
- Reflect on the **robustness, efficiency, and parameter sensitivity** of various methods.

---

## Tools & Libraries
- **Python**
- **OpenCV**
- **NumPy / Matplotlib**

---

## Assignments

### **Task 1: Harris Corner Detector**
**Objective:** Implement and evaluate Harris corner detection.  
**Resource:** `left.jpg`

**Instructions:**
1. Implement `harris_corners.m` (or `.py`) to detect corners.  
2. Rotate the image by 45° and reapply the detector — analyze **rotation invariance**.  
3. Scale the image and observe corner detection behavior — analyze **scale sensitivity**.  
4. Compare your implementation with **OpenCV’s built-in Harris detector**.  
5. Experiment with **parameter tuning** (e.g., k, σ, threshold, NMS window size).

---

### **Task 2: Feature Detection and Matching**
**Objective:** Compare **SIFT** and **Harris** features across image pairs.  
**Resources:**  
- Pair 1: `left.jpg`, `right.jpg`  
- Pair 2: `notre_dame1.jpg`, `notre_dame2.jpg`

**Instructions:**
1. Detect features using **SIFT** and **Harris** detectors.  
2. Extract descriptors (e.g., SIFT or Harris+SIFT combination).  
3. Match features between image pairs and **visualize correspondences**.  
4. Compare match quality using **RANSAC (F-RANSAC vs. H-RANSAC)** for geometric verification.

---

### **Task 3: Robotic Scenario – Stereo Matching**
**Objective:** Apply feature matching to **stereo video feeds** in robotic applications.  
**Resources:**  
- **Custom Dataset:** Boston Dynamics Spot  
- **Custom Dataset:** PennCOSYVIO

**Instructions:**
1. Implement **real-time feature matching** between left/right image pairs.  
2. Compute performance metrics:

- N_total — total features in the left image  
- N_valid — number of geometrically valid matches  
- N_failed = N_total − N_valid

   Also measure:
   - Frames per second (FPS)
   - Average number of matched features
   - Number of failed matches

3. Visualize matches for a representative frame.

---

## Reflection
This lab demonstrates how **feature detection and matching** underpin many real-world computer vision and robotics tasks.  
Through systematic experimentation, we gain insights into how detector design, descriptor choice, and geometric models affect both **accuracy** and **real-time performance**.

---
