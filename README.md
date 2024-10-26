
---

# 📸 Image Entity Extraction

## 📝 Problem Statement
In the training data, we have the following columns:
- 🖼️ **Image Link**
- 🆔 **Group ID**
- 🏷️ **Entity Name**
- 🎯 **Target Column**: **Entity Value**

Our goal is to extract the **entity value** (e.g., `10gm`, `10W`, `10cm`, etc.) from the pictures with the correct units.

## 🚀 Approach

1. **Image Preprocessing**:  
   We started by preprocessing the images to enhance text clarity.

2. **🧠 Keras for Number & Unit Detection**:  
   We used [Keras OCR](https://github.com/faustomorales/keras-ocr) to detect both numbers and units like `g`, `W`, and `cm`.

3. **🔍 Text Extraction with Pytesseract**:  
   We passed specific cross-section images to [Pytesseract](https://github.com/madmaze/pytesseract), ensuring it captured text, including decimal points accurately.

4. **📜 Natural Language Processing**:  
   After detecting the text from images, we applied **Natural Language Processing** using the [DeBERTa Transformer](https://github.com/microsoft/DeBERTa) to further analyze and extract the correct entity values.

5. **💡 Model Output**:  
   The final result was obtained after processing the image through **DeBERTa**, giving us the entity value.

## 📊 Results
- **Accuracy**: We achieved **68%** accuracy in extracting the correct entity values.
  
## ⚠️ Demerits
- **⏳ Processing Time**: The time to process each image is relatively high, averaging **1.21 seconds per image**.

---

Let me know if you'd like further adjustments! 😊
