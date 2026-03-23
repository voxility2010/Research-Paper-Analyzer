# Research Paper Analyzer with LLM & Multilingual Translation

> Intelligently analyze research papers, simplify complex content using LLMs, and translate results into regional languages — without reading the entire document.

---

## Overview

This project builds an end-to-end NLP pipeline that processes research papers in PDF format. It extracts key information, generates chunk-wise summaries using a language model (FLAN-T5), and translates the output into user-selected Indian regional languages via the Sarvam AI API.

---

## Features

- Extracts **Title** and **Abstract** from research PDFs
- Cleans noisy PDF text (removes metadata, author info, etc.)
- Splits abstract into **sentence-based chunks**
- Generates **chunk-wise summaries** using LLM (FLAN-T5)
- Converts summaries into **structured bullet points**
- **Translates** title and each summary bullet into a user-selected language using Sarvam AI
- Handles API input constraints using **chunk-based translation**

---

## Pipeline

```
PDF → Text Extraction → Cleaning → Chunking
    → LLM Summarization (per chunk)
    → Bullet Point Generation
    → Translation (Sarvam AI, chunk-wise)
```

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| PyMuPDF | PDF text extraction |
| Hugging Face Transformers (FLAN-T5) | Text summarization |
| Sarvam AI API | Multilingual translation |
| Regex / Text Processing | Cleaning & segmentation |

---

## Project Structure

```
├── notebook.ipynb   # Main pipeline notebook
└── README.md
```

---

## Setup Instructions

### 1. Install Dependencies

```bash
pip install pymupdf transformers sarvamai
```

### 2. Set Sarvam API Key

```bash
export SARVAM_API_KEY="your_api_key_here"
```

### 3. Run the Notebook

- Upload a research paper PDF
- Run cells sequentially
- Enter your preferred language when prompted (e.g., `hindi`, `tamil`, `bengali`)

---

## Supported Languages

| Language | Code |
|---|---|
| Hindi | `hi-IN` |
| Tamil | `ta-IN` |
| Bengali | `bn-IN` |
| Telugu | `te-IN` |
| Gujarati | `gu-IN` |

> User-friendly input like `"hindi"` is automatically mapped to the correct API format.

---

## Sample Output

```
TITLE (ENGLISH):
Attention Is All You Need

TITLE (TRANSLATED):
सारा ध्यान ही पर्याप्त है

ENGLISH SUMMARY:
- Transformer replaces RNN/CNN with attention mechanism
- Improves translation performance and efficiency
- Enables faster parallel training
- Achieves state-of-the-art results

TRANSLATED SUMMARY:
- ट्रांसफॉर्मर ध्यान तंत्र का उपयोग करता है
- प्रदर्शन और प्रशिक्षण दक्षता में सुधार करता है
- प्रशिक्षण को तेज़ बनाता है
- अत्याधुनिक परिणाम प्राप्त करता है
```

---

## Key Highlights

- Uses **semantic understanding (LLM)** instead of basic text parsing
- Implements **chunk-wise summarization** for long documents
- Maintains **structured output** across languages
- Handles real-world **API input constraints**
- Demonstrates a complete **end-to-end NLP pipeline**

---

## Future Improvements

- [ ] Full research paper summarization (beyond abstract)
- [ ] Table and figure extraction
- [ ] Web-based UI for easier usage
- [ ] Support for more regional languages
- [ ] Document comparison between paper versions

---

## Use Cases

- Students understanding research papers quickly
- Researchers conducting rapid literature reviews
- Multilingual access to technical content
- Educational tools for non-expert audiences

---

## Contributing

Contributions are welcome! Feel free to fork this repository, open issues, or submit pull requests to enhance the project.

---

## Contact:
Vardha Kathuria
vardhakathuria@gmail.com

For queries or collaboration opportunities, feel free to connect.
