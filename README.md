
# AI Attention Visualizer

An interactive AI application that extracts text from uploaded images and visualizes how an attention mechanism identifies important words in the extracted text.

## Overview

**AI Attention Visualizer** demonstrates the complete workflow of processing text through OCR, generating semantic embeddings, calculating attention scores, and identifying the words that receive the highest attention.

The application provides a simple Streamlit interface where users can upload an image containing text and explore the resulting attention information.

## Features

* Upload images containing text
* Extract text using OCR
* Generate text embeddings using Sentence Transformers
* Calculate attention scores using Query, Key, and Value representations
* Apply Softmax to obtain attention weights
* Identify the highest-attention word
* Visualize attention results interactively
* Simple web interface using Streamlit

## Project Workflow

```text
Image
  ↓
OCR
  ↓
Extracted Text
  ↓
Tokenization
  ↓
Sentence Embeddings
  ↓
Query, Key, Value
  ↓
Attention Scores
  ↓
Softmax
  ↓
Attention Weights
  ↓
Attention Visualization
```

## Technologies Used

| Technology            | Purpose                       |
| --------------------- | ----------------------------- |
| Python                | Core programming              |
| Streamlit             | Interactive web application   |
| Pytesseract           | Optical Character Recognition |
| Pillow                | Image processing              |
| NumPy                 | Numerical computation         |
| Sentence Transformers | Text embeddings               |
| Matplotlib            | Visualization                 |

## Project Structure

```text
AI-Attention-Visualizer/
│
├── app.py
├── attention.py
├── embedding.py
├── ocr.py
├── requirements.txt
└── README.md
```

### `app.py`

Main Streamlit application that connects all components and provides the user interface.

### `ocr.py`

Extracts text from uploaded images using OCR.

### `embedding.py`

Converts extracted text into numerical embeddings using a Sentence Transformer model.

### `attention.py`

Implements the attention mechanism and calculates attention scores and weights.

## Attention Mechanism

The project demonstrates the basic attention workflow:

```text
Input Embeddings
       ↓
   Query (Q)
   Key (K)
   Value (V)
       ↓
 Q × Kᵀ
       ↓
 Scaling
       ↓
 Softmax
       ↓
Attention Weights
       ↓
Weighted Values
       ↓
Attention Output
```

The attention score can be represented as:

```text
Attention(Q,K,V) =
softmax(QKᵀ / √dₖ)V
```

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/AI-Attention-Visualizer.git
```

### 2. Open the project

```bash
cd AI-Attention-Visualizer
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python -m streamlit run app.py
```

Running Streamlit as `python -m streamlit run app.py` is an official supported way to launch a Streamlit application. ([Streamlit Docs][2])

## Example

The user uploads an image containing text:

```text
Artificial Intelligence is changing
the way we interact with technology.
```

The application then:

```text
Image
 ↓
OCR
 ↓
"Artificial Intelligence is changing..."
 ↓
Embeddings
 ↓
Attention Calculation
 ↓
Attention Visualization
```

The visualization helps demonstrate which words receive higher attention scores.

## Applications

* Understanding attention mechanisms
* NLP education and demonstrations
* OCR-based text analysis
* Semantic text processing
* Machine learning visualization
* Transformer architecture learning

## Future Enhancements

* Multi-head attention visualization
* Interactive attention heatmaps
* Support for multiple languages
* PDF document input
* Downloadable attention reports
* Transformer-based attention comparison

## Author

**Varalakshmi Karthick Kumar**

B.Sc. Computer Science with AI
