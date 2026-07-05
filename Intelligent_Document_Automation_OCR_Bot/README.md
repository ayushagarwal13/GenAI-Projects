# 📄 Intelligent Document Automation using OCR and Gemini AI

An end-to-end **Generative AI + Computer Vision** project that automates information extraction from receipt images. The system uses **OpenCV** for image preprocessing, **Tesseract OCR** for text extraction, and **Google Gemini AI** to convert unstructured OCR text into structured JSON data.

This project demonstrates how traditional OCR can be combined with Large Language Models (LLMs) to build an Intelligent Document Processing (IDP) pipeline.

---

## 🚀 Project Overview

Organizations process thousands of invoices, receipts, bills, and forms every day. Manually entering information from these documents into databases is slow, expensive, and prone to human error.

This project automates the complete workflow by:

- Reading receipt images
- Preprocessing images using OpenCV
- Extracting text using Tesseract OCR
- Understanding extracted text using Gemini AI
- Returning structured JSON output

---

## 🎯 Problem Statement

Businesses receive large volumes of document images such as receipts and invoices every day. Manual data entry is time-consuming and error-prone.

The objective of this project is to automate document understanding by extracting text using OCR and converting the extracted text into structured JSON using Google's Gemini Large Language Model.

---

## 🏗️ Project Pipeline

```
Receipt Image
       │
       ▼
OpenCV Image Preprocessing
       │
       ▼
Tesseract OCR
       │
       ▼
Raw Extracted Text
       │
       ▼
Gemini AI
       │
       ▼
Structured JSON Output
```

---

# 📂 Dataset

**SROIE 2019 - Scanned Receipts OCR and Information Extraction Dataset**

Dataset contains:

- Receipt Images
- Bounding Box Annotations
- Ground Truth Entity Files

For this project, only the receipt images are used as input.

---

# 🛠️ Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Tesseract OCR
- pytesseract
- Google Gemini API
- Google Colab

---

# 🧠 Concepts Covered

- Optical Character Recognition (OCR)
- Intelligent Document Processing (IDP)
- Image Preprocessing
- Grayscale Conversion
- Thresholding
- Text Extraction
- Prompt Engineering
- Structured Information Extraction
- JSON Generation
- Generative AI

---

# ⚙️ Workflow

### Step 1

Load receipt image.

### Step 2

Preprocess image using OpenCV.

- Read Image
- Convert to Grayscale
- Apply Thresholding

### Step 3

Extract text using Tesseract OCR.

Example:

```
RESTORAN WAN SHENG

TOTAL : 4.80

GST : 0.26
```

### Step 4

Send OCR text to Gemini AI.

Prompt:

```
Extract the following information:

- Company Name
- Invoice Number
- Date
- Time
- Total Amount
- GST Amount

Return only JSON.
```

### Step 5

Gemini converts unstructured OCR text into structured JSON.

Example Output:

```json
{
  "company_name": "RESTORAN WAN SHENG",
  "invoice_number": "1064250",
  "date": "21-03-2018",
  "time": "11:42:20",
  "total_amount": 4.80,
  "gst_amount": 0.26
}
```

---

# 📁 Project Structure

```
Intelligent-Document-Automation/

│
├── Intelligent_Document_Automation.ipynb
├── README.md
├── requirements.txt
└── images/
```

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/ayushagarwal13/Intelligent_Document_Automation_OCR_Bot.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Install Tesseract

```bash
sudo apt install tesseract-ocr
```

---

# 🔑 Configure Gemini API

Create a Google AI Studio API Key.

In Google Colab:

```python
from google.colab import userdata

api_key = userdata.get("GOOGLE_API_KEY")
```

Initialize Gemini client.

---

# 🤖 Gemini Model Used

**Model**

```
gemini-2.5-flash
```

Gemini is responsible for:

- Understanding OCR text
- Identifying important entities
- Extracting business information
- Returning structured JSON

Unlike OCR, Gemini understands the meaning of the extracted text instead of simply reading characters.

---

# 📊 Sample Output

### OCR Output

```
RESTORAN WAN SHENG

Date : 21-03-2018

GST : 0.26

TOTAL : 4.80
```

### Gemini Output

```json
{
  "company_name": "RESTORAN WAN SHENG",
  "invoice_number": "1064250",
  "date": "21-03-2018",
  "time": "11:42:20",
  "total_amount": 4.80,
  "gst_amount": 0.26
}
```

---

# 💡 Features

- Receipt Image Processing
- OCR using Tesseract
- Image Preprocessing using OpenCV
- Automatic Text Extraction
- LLM-powered Information Extraction
- Structured JSON Output
- Easy to Extend for Invoices, Bills, and Forms

---

# 🚀 Future Improvements

- Batch Processing
- PDF Support
- Invoice Processing
- Multi-language OCR
- Receipt Classification
- Database Integration
- Streamlit Web Application
- REST API using FastAPI

---

# 📚 Learning Outcomes

This project demonstrates practical knowledge of:

- Computer Vision
- OCR
- Intelligent Document Processing
- Prompt Engineering
- Google Gemini API
- OpenCV
- Generative AI Applications

---

# 🎥 YouTube Demo

A complete explanation of this project is available on my YouTube channel, where I explain every step from image preprocessing to structured JSON generation.

---

# ⭐ If you found this project helpful

Please consider giving this repository a ⭐ on GitHub.
