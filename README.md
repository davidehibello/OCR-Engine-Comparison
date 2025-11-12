# 🧾 OCR Engine Comparison on Mortgage Documents

This project benchmarks three leading OCR engines — **Tesseract OCR**, **PaddleOCR**, and **EasyOCR** — on a scanned mortgage document.  
It demonstrates how preprocessing, model selection, and layout handling affect OCR accuracy, making it a practical workflow for GenAI and data extraction systems.

---

## 🚀 Features
- 📄 Extract text from scanned PDFs using three OCR engines.  
- 🧠 Evaluate text accuracy, structure preservation, and layout interpretation.  
- 🖼️ Visualize bounding boxes to inspect word-level OCR performance.  
- ⚙️ Apply OpenCV preprocessing (thresholding, resizing, denoising) to boost accuracy.  
- 🔍 Compare structured vs. unstructured output for downstream AI readiness.

---

## 🧰 Tech Stack
- **Languages:** Python  
- **Libraries:** PyMuPDF, OpenCV, Pillow, Tesseract, PaddleOCR, EasyOCR  
- **Tools:** Google Colab, pdf2image, NumPy, Matplotlib  

---

## 🧠 Project Workflow

### 1️⃣ Tesseract OCR
- Extracted text using `pytesseract` after grayscale conversion and thresholding.  
- Applied bounding boxes and filtering for high-confidence text segments.  
- Cleaned and formatted text output for consistency.

### 2️⃣ PaddleOCR
- Processed PDFs with `pdf2image` for image conversion.  
- Used `PaddleOCR` for structured text extraction and layout preservation.  
- Visualized results with annotated bounding boxes and confidence scores.

### 3️⃣ EasyOCR
- Extracted multi-language text segments with confidence scoring.  
- Compared detection density and formatting consistency with other engines.

---

## 🔬 Observations
- **Tesseract** performed best on clean, preprocessed text but struggled with layout-heavy sections.  
- **PaddleOCR** provided superior structure retention and bounding accuracy, ideal for tables and forms.  
- **EasyOCR** achieved balanced results and fast runtime with minimal setup.  
- Combining OCRs can improve downstream AI training datasets by blending structural and textual accuracy.

---

## 📦 Installation
```bash
pip install pytesseract paddleocr easyocr pymupdf opencv-python pillow pdf2image
sudo apt install tesseract-ocr poppler-utils
```
💻 Usage

Upload your scanned PDF in Google Colab or your local environment, then run:
```bash
python compare_ocr.py
```

