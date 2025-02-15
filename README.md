# Computer Vision Color Research on Luxury Car Brands

## 📌 Project Overview
This project focuses on separating an image's foreground and background in **Python** and computing the corresponding **color values (Hue, Saturation, Value - HSV)** for both. By leveraging **OpenCV** and **image processing techniques**, the project aims to analyze and quantify image colorfulness.

## 🚀 Features
- **Foreground and Background Segmentation** – Extract distinct layers from images.
- **HSV Color Analysis** – Compute hue, saturation, and value for each segment.
- **Colorfulness Calculation** – Quantify how colorful the image and its components are.
- **Batch Image Processing** – Analyze large datasets efficiently.
- **Visualization Tools** – Generate masked and segmented images.

## 📂 Directory Structure
```
📦 Computer_Vision_Color_Research
 ┣ 📂 data             # Image dataset used for analysis
 ┣ 📂 notebooks        # Jupyter/Colab notebooks for processing and visualization
 ┣ 📂 scripts          # Python scripts for batch processing
 ┣ 📜 ColorSeparating.ipynb  # Main notebook for foreground-background separation
 ┣ 📜 README.md        # Project documentation (this file)
```

## 🛠️ Installation & Setup
To run this project, ensure you have the following dependencies installed:
```sh
pip install numpy matplotlib opencv-python imutils pandas
```

If using Google Colab, mount Google Drive to access stored images:
```python
from google.colab import drive
drive.mount('/content/gdrive')
```

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
  
  \[ C = \sqrt{rbStd^2 + ybStd^2} + 0.3 * \sqrt{rbMean^2 + ybMean^2} \]

## 📜 Example Output
| Image  | Foreground Hue | Background Hue | Colorfulness |
|--------|---------------|---------------|--------------|
| Image1 | 83.02         | 72.45         | 134.33       |
| Image2 | 102.49        | 43.01         | 158.21       |

## 📈 Visualization Examples
- **Foreground and Background Separation:**
  - <img width="461" alt="Screenshot 2025-02-14 at 10 10 44 PM" src="https://github.com/user-attachments/assets/152fbcb5-7d9e-49d2-9313-6ea983b3bdae" />

  - <img width="442" alt="Screenshot 2025-02-14 at 10 10 51 PM" src="https://github.com/user-attachments/assets/00c18fcd-9241-4add-838f-35b0003af261" />
  - <img width="444" alt="Screenshot 2025-02-14 at 10 11 01 PM" src="https://github.com/user-attachments/assets/33b1b84b-1faa-4852-947f-89cd56812253" />


- **Colorfulness Score Comparisons (one example output)**
  - <img width="353" alt="Screenshot 2025-02-14 at 10 12 18 PM" src="https://github.com/user-attachments/assets/91d87182-013f-482c-a0f9-fbc72055518c" />

## 🔍 Future Enhancements
- **Apply Deep Learning** for better segmentation.
- **Expand Dataset** for improved generalization.
- **Develop a Web Interface** for interactive image processing.

---
**Computer Vision Color Research** - A project analyzing image segmentation and color extraction using OpenCV. 🚀

