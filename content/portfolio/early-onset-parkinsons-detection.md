+++
categories = ["ai"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Deep learning model using CNNs to detect early-onset Parkinson’s from speech data"
image = "https://ik.imagekit.io/ys4gkaixy/Neural_network.svg?updatedAt=1744744987487"
title = "Early Onset Parkinson's Detection from Speech Data"
type = "post"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Python_logo_01.svg?updatedAt=1744511052787"
name = "Python"
url = "https://www.python.org/"
[[tech]]
name = "TensorFlow"
url = "https://www.tensorflow.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg"
[[tech]]
name = "Librosa"
url = "https://librosa.org/"
logo = "https://ik.imagekit.io/ys4gkaixy/With%20Name%20logos/librosa-logo.svg?updatedAt=1744660100000"
[[tech]]
name = "CNN"
url = "https://en.wikipedia.org/wiki/Convolutional_neural_network"
logo = "https://www.svgrepo.com/show/498636/neural-network.svg"
+++

## Overview

This project implements an end-to-end deep learning model using convolutional neural networks (CNNs) to detect early-onset Parkinson’s Disease (PD) from speech data. Leveraging Mel spectrograms and advanced preprocessing, the model aims to identify subtle vocal indicators of PD.

The work builds on methodologies by Quan et al. and evaluates their applicability to a real-world Italian dataset. Tools such as **Librosa** for audio processing and **NeuroSpeech** for feature exploration played a crucial role in the pipeline.

This project was completed as part of graduate coursework funded by an international collaboration grant. The work involved partnership with a researcher from [Indian Hospital/Institution Name, if allowed], enabling access to multilingual clinical datasets and expert insights on Parkinson’s speech biomarkers

---

## Motivation

Early-onset PD presents challenges in detection due to its subtle symptoms. Since ~90% of PD patients experience speech impairments, analyzing vocal characteristics becomes a valuable non-invasive biomarker.

---

## Techniques Used

- **CNN-based model** with:
  - Time-distributed 2D CNN for local frequency analysis
  - 1D CNN for temporal dependencies
- **Mel-spectrograms** used as image-like inputs
- **Librosa** for audio processing
- **NeuroSpeech** for comparative speech analysis
- **Datasets** in Italian, Telugu, and English

---

## Dataset

- **Italian Dataset**: 394 HC samples and 437 PD samples from 65 participants.
- **Telugu Dataset**: 24 samples from 8 participants under varied noise conditions.
- **English Dataset**: KCL Hospital phone-based recordings with detailed PD annotations.

---

## Tools & Libraries

- Python
- TensorFlow / Keras
- Librosa
- NeuroSpeech
- Matplotlib / Seaborn (for visualization)

---

## Results

- Achieved **98% validation accuracy** on Italian speech samples using improved preprocessing (2,000-frame spectrogram segments).
- Found **low-frequency spectrogram features** to be most indicative of PD.
- Cross-language testing showed poor generalizability, emphasizing the need for **language-specific models**.

---

## Challenges & Insights

- CNNs are powerful but lack interpretability — a concern in clinical contexts.
- Cross-language models fail without balanced training data.
- Future improvements include:
  - Expanding training sets for multilingual support
  - Exploring interpretable AI methods
  - Augmenting with prosody and intelligibility features

---

## References

- [Quan et al., 2022: *End-to-End Deep Learning for PD Speech Detection*](https://www.sciencedirect.com/science/article/abs/pii/S0208521622000341)
- [Dimauro & Girardi, 2019: *Italian Parkinson’s Voice and Speech Dataset*](https://ieee-dataport.org/open-access/italian-parkinsons-voice-and-speech)
- [Orozco-Arroyave et al., 2018: *NeuroSpeech Tool*](https://www.sciencedirect.com/science/article/pii/S105120041730146X)
- [Jaeger et al., 2019: *KCL English Dataset (MDVR-KCL)*](https://explore.openaire.eu/search/dataset?pid=10.5281%2Fzenodo.2867215)


---

## Takeaway

This project shows that **deep learning can detect early-onset Parkinson’s from speech** with high accuracy on single-language data. With better datasets and interpretability tools, speech-based diagnostics may become a reality.