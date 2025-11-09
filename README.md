
---

# 📸 Image Entity Extraction

## 📝 Problem Statement
In the training data, we have the following columns:
- 🖼️ **Image Link**
- 🆔 **Group ID**
- 🏷️ **Entity Name**
- 🎯 **Target Column**: Entity Value

The objective is to identify and extract numerical entity values with their respective units (e.g., 10gm, 10W, 10cm) directly from images.

## 🚀 Approach

1. **Image Preprocessing**:  
   Images were preprocessed to enhance clarity and improve text detection accuracy.

2. **🔠 OCR-Based Detection**:  
   [Keras OCR](https://github.com/faustomorales/keras-ocr) was used to detect numeric values and units (g, W, cm), while Pytesseract extracted detailed text including decimals from refined image sections.
   
4. **🔍 Text Extraction with Pytesseract**:  
   I passed specific cross-section images to [Pytesseract](https://github.com/madmaze/pytesseract), ensuring it captured text, including decimal points accurately.

5. **🧠 NLP Analysis**:  
   The extracted text was processed using the [DeBERTa Transformer](https://github.com/microsoft/DeBERTa) to accurately identify and extract the correct entity values.

6. **💡 Model Output**:  
   The pipeline produced precise entity values by combining visual and textual data understanding.

## 📊 Results
- **Accuracy**: **68%** accuracy in extracting the correct entity values.
- **Average Processing Time:** 1.21 seconds per image
  
## ⚠️ Limitation
- The model’s main drawback is its relatively high processing time per image.


