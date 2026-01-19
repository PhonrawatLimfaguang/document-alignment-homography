# 📄 Document Alignment using Homography
> **Perspective correction and document restoration using OpenCV & Feature Matching**

This project focuses on transforming skewed or tilted document images into high-quality, "top-down" scanned views. Developed for the **DE461 Introduction to Computer Vision** course, it explores the mathematical foundation of **Homography** and compares various detection techniques.

<img width="1013" height="2990" alt="image" src="https://github.com/user-attachments/assets/59ec4a33-c6c8-4120-9cfb-68f3f155f039" />

---

## 🛠️ Implementation Pipeline
1. **Image Preprocessing:** - Applied **CLAHE** (Contrast Limited Adaptive Histogram Equalization) to handle uneven lighting.
   - Used **Gaussian Blur** and **Adaptive Thresholding** to prepare images for edge detection.
2. **Alignment Methods:**
   - **Contour-based:** Detects the largest quadrilateral for quick 4-point perspective transforms.
   - **ORB + RANSAC:** A robust feature-based approach that matches document keypoints even with complex backgrounds.
3. **Evaluation Metrics:** Used **SSIM** (Structural Similarity) and **PSNR** to measure the accuracy of the restored documents.

---

## 📈 Performance & Results
Based on our experimental data in `data/results.csv`:
* **Preprocessing Impact:** The integration of CLAHE significantly improved the **Inlier Ratio** for feature matching in low-light environments.
* **Accuracy:** ORB + RANSAC provided more stable Homography matrices compared to simple contour detection when document edges were partially obstructed.
* **Visual Improvement:** Achieved higher **SSIM scores** (up to ~0.70+) after applying perspective correction.
<img width="668" height="526" alt="image" src="https://github.com/user-attachments/assets/12174bc2-152a-4331-a2ee-045711b311ae" />
<img width="668" height="526" alt="image" src="https://github.com/user-attachments/assets/114c2e94-32b0-4bc0-aa82-bd7f4cc1fe8d" />

---

## 📁 Repository Structure
* **`data/`**: Performance logs and metric comparisons (`results.csv`).
* **`notebooks/`**: Full Python implementation including preprocessing and evaluation.
* **`report/`**: Detailed academic report with mathematical derivations.

---

## 🛠️ Tech Stack
* **OpenCV:** Core CV operations (Homography, ORB, FindContours).
* **Scikit-image:** Performance evaluation (SSIM, PSNR).
* **NumPy & Pandas:** Matrix calculations and data logging.

---
