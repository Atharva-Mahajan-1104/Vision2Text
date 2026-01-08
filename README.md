
# 🌌 Vision2Text

### Teaching Machines to See — and Speak

> *An artistic exploration of how images become language through deep learning.*

---

![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-CNN-blue)
![NLP](https://img.shields.io/badge/NLP-LSTM-green)
![Status](https://img.shields.io/badge/Project-Active-success)

---

## ✨ The Idea

Humans don’t just **see** images — we *understand* them, describe them, and attach meaning through language.
**Vision2Text** is a project that explores how machines can do the same.

By blending **visual perception** and **language generation**, this system learns to translate pixels into words.
An image passes through a visual encoder that captures *what is present*, and a language model that decides *how to say it*.

The result is a model that doesn’t just classify images — it **narrates them**.

---

## 🎨 What This Project Explores

* How visual features can be transformed into language
* How sequential models learn grammar from context
* How meaning emerges from multimodal learning
* The balance between engineering precision and creative output

This repository is equal parts **engineering artifact** and **creative experiment**.

---

## 🧠 How It Works (Conceptually)

```text
Light → Pixels → Features → Words → Meaning
```

1. **Vision**
   A pretrained CNN (ResNet-50) extracts rich semantic features from an image.

2. **Memory**
   These features seed an LSTM that learns how words follow one another.

3. **Language**
   The model generates captions one token at a time — learning grammar, structure, and semantics.

4. **Evaluation**
   Captions are evaluated using BLEU scores to measure closeness to human descriptions.

---

## 🧩 Architecture Overview

```text
[ Image ]
    ↓
[ CNN Encoder (ResNet-50) ]
    ↓
[ Visual Embedding ]
    ↓
[ LSTM Decoder ]
    ↓
[ Generated Caption ]
```

* The CNN backbone is frozen for stability
* The decoder is trained with teacher forcing
* Cross-entropy loss guides language learning

---

## ✨ Core Features

* Pretrained **ResNet-50** encoder (transfer learning)
* LSTM decoder with embeddings & dropout
* Vocabulary construction with frequency control
* Teacher forcing during training
* BLEU-1 → BLEU-4 evaluation
* Automatic visualization of training dynamics
* Saved artifacts for reproducibility & inference

---


## 📊 Visual Output

Training automatically produces:

* 📉 Loss curves (learning dynamics)
* 📈 BLEU score progression (caption quality)
* 🖼️ Example captions generated from unseen images

Each run leaves behind a **story of learning** — not just numbers.

---

## 🚀 Training the Model

```bash
python src/train.py \
  --captions data/captions.csv \
  --images-root data \
  --outdir outputs \
  --epochs 10 \
  --batch-size 64 \
  --embed-dim 256 \
  --hidden-dim 512 \
  --min-freq 1 \
  --max-len 20
```

---

## 🔍 Inference: Let the Model Speak

```bash
python src/infer.py \
  --checkpoint outputs/best_captioner.pt \
  --vocab outputs/vocab.json \
  --image data/images/example1.jpg
```

The model observes the image — then responds with language it has learned.

---

## 📈 What the Results Tell Us

* Caption fluency improves steadily with training
* Larger datasets significantly enhance semantic richness
* Freezing CNN layers stabilizes early learning
* Language generation quality is tightly coupled with vocabulary design

---

## 🌱 Future Directions

* Attention mechanisms for spatial focus
* Beam search for richer captions
* Transformer-based decoders
* Larger datasets (MSCOCO scale)
* Human evaluation alongside BLEU metrics

---

## 🧠 Why This Project Matters

Vision2Text represents more than a model — it demonstrates:

* Multimodal reasoning
* Practical deep learning system design
* Reproducible experimentation
* The intersection of perception and language

---

