# Computer Vision Color Research

## 📌 Project Overview

This project focuses on separating an image's foreground and background in **Python** and **computing the corresponding color values (Hue, Saturation, Value - HSV)** for both. By leveraging **OpenCV and image processing techniques**, the project aims to analyze and quantify image colorfulness. This work was conducted under the guidance of Professor Jeffrey Lee as part of a research study on luxury product color-pricing analysis from 2022 Fall to 2023 Spring.


## 🚀 Features
- **Foreground and Background Segmentation** – Extract distinct layers from images.
- **HSV Color Analysis** – Compute hue, saturation, and value for each segment.
- **Colorfulness Calculation** – Quantify how colorful the image and its components are.
- **Batch Image Processing** – Analyze large datasets efficiently.
- **Visualization Tools** – Generate masked and segmented images.


## 🖼️ How It Works
1. **Load Images:** Extract images from a specified directory.
2. **Convert to Grayscale:** Use OpenCV to apply thresholding.
3. **Generate Masks:** Identify foreground and background regions.
4. **Extract Features:** Compute color values (HSV) and colorfulness score.
5. **Save Results:** Export results to a structured dataset (CSV/Excel).

## 📊 Image Processing Example
```python
# Convert image to grayscale
image = cv2.imread("image.png")
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply threshold to segment foreground/background
ret, mask = cv2.threshold(gray, 0, 255, cv2.THRESH_BINARY_INV + cv2.THRESH_OTSU)
```

## 🎯 Key Algorithms & Techniques
- **Thresholding & Masking:** Binary thresholding for background/foreground segmentation.
- **Color Space Conversion:** Convert images to HSV for color analysis.
- **Feature Extraction:** Compute mean hue, saturation, and value for both layers.
- **Colorfulness Metric:** Use the metric:
  <img width="526" alt="Screenshot 2025-02-14 at 10 15 16 PM" src="https://github.com/user-attachments/assets/f2c0f261-dd5a-49c4-8e04-4a3eaf0523b2" />


## 📈 Visualization Examples
- **Foreground and Background Separation:**
  - <img width="461" alt="Screenshot 2025-02-14 at 10 10 44 PM" src="https://github.com/user-attachments/assets/152fbcb5-7d9e-49d2-9313-6ea983b3bdae" />

  - <img width="442" alt="Screenshot 2025-02-14 at 10 10 51 PM" src="https://github.com/user-attachments/assets/00c18fcd-9241-4add-838f-35b0003af261" />
  - <img width="444" alt="Screenshot 2025-02-14 at 10 11 01 PM" src="https://github.com/user-attachments/assets/33b1b84b-1faa-4852-947f-89cd56812253" />


- **Colorfulness Score Comparisons (one example output)**
  - <img width="353" alt="Screenshot 2025-02-14 at 10 12 18 PM" src="https://github.com/user-attachments/assets/91d87182-013f-482c-a0f9-fbc72055518c" />

---


