# AdaIN Neural Style Transfer

Real-time arbitrary neural style transfer web application built using PyTorch and Flask.

This project implements **Adaptive Instance Normalization (AdaIN)** to transfer artistic styles from one image onto another while preserving the structural content of the original image. The system performs fast feed-forward style transfer and provides an interactive web interface for generating stylized outputs in real time.

---

# Demo Preview

## Example 1

| Content Image | Style Image | Stylized Output |
|---|---|---|
| ![](examples/brad_pitt.jpg) | ![](examples/sketch.png) | ![](examples/stylized_brad_pitt.jpg) |

---

## Example 2

| Content Image | Style Image | Stylized Output |
|---|---|---|
| ![](examples/brad_pitt.jpg) | ![](examples/picasso_seated_nude_hr.jpg) | ![](examples/stylized_brad_pitt%20(1).jpg) |

---

# Features

- Real-time arbitrary neural style transfer
- AdaIN-based feature alignment for flexible style adaptation
- Interactive web interface using Flask
- Adjustable style intensity control
- Upload or capture images directly from device camera
- Feed-forward inference for fast stylization
- Responsive futuristic UI with live previews
- Supports multiple artistic domains:
  - sketch
  - watercolor
  - cubism
  - abstract art
  - digital painting
  - anime-style textures
  - classical artwork

---

# How It Works

The system follows an encoder-transformer-decoder pipeline:

1. The **content image** and **style image** are passed through a pretrained VGG encoder.
2. Deep feature representations are extracted from both images.
3. Adaptive Instance Normalization (AdaIN) aligns the statistical properties of content features with style features.
4. A trained decoder reconstructs the transformed feature map into a stylized image.

---

# Project Architecture

```text
Content Image ─────┐
                   │
                   ▼
            VGG Encoder
                   │
                   │
Style Image ───────┘
                   │
                   ▼
      Adaptive Instance
        Normalization
             (AdaIN)
                   │
                   ▼
          Decoder Network
                   │
                   ▼
          Stylized Output
```

---

# Tech Stack

## Deep Learning

- PyTorch
- Adaptive Instance Normalization (AdaIN)
- VGG-19 Encoder
- Encoder-Decoder Architecture

## Backend

- Flask

## Frontend

- HTML5
- CSS3
- Bootstrap 5
- JavaScript

---

# Installation

Clone the repository:

```bash
git clone https://github.com/kumarritik8923/adain-neural-style-transfer.git
```

Move into project directory:

```bash
cd adain-neural-style-transfer
```

Create virtual environment:

```bash
python -m venv myenv
```

Activate environment:

### Windows

```bash
myenv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
python app.py
```

---

# Folder Structure

```text
adain-neural-style-transfer/
│
├── templates/
│   └── index.html
│
├── static/
│
├── examples/
│
├── utils/
│
├── app.py
├── decoder.pth
├── vgg_normalised.pth
├── requirements.txt
├── Procfile
└── README.md
```
