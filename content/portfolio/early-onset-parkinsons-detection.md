+++
categories = ["ai"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Deep learning model using CNNs to detect early-onset Parkinson’s from speech data"
image = "https://ik.imagekit.io/ys4gkaixy/Artificial_neural_network.svg?updatedAt=1745129381637"
title = "Early Onset Parkinson's Detection from Speech Data"
type = "post"
weight=2
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Python_logo_01.svg?updatedAt=1744511052787"
name = "Python"
url = "https://www.python.org/"
[[tech]]
name = "Keras"
url = "https://keras.io"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/keras/keras-original.svg"
[[tech]]
name = "Librosa"
url = "https://librosa.org/"
logo = "https://ik.imagekit.io/ys4gkaixy/sound-waves-svgrepo-com.svg?updatedAt=1745129088650"
[[tech]]
name = "CNN"
url = "https://en.wikipedia.org/wiki/Convolutional_neural_network"
logo = "https://ik.imagekit.io/ys4gkaixy/Neural_network.svg?updatedAt=1744744987487"
+++

## **Overview**

This project implements an end-to-end deep learning model using **convolutional neural networks (CNNs)** to detect **early-onset Parkinson's Disease (PD)** from speech data. By leveraging **Mel spectrograms**—visual and mathematical representations of sound frequencies over time, to reflect human hearing perception—our model extracts features that help identify vocal indicators of PD. 

The work builds on methodologies by Quan et al. and evaluates their applicability to a real-world Italian dataset. Tools like **Librosa** were used for audio processing, and **NeuroSpeech**, a software tool designed to assist medical professionals in evaluating biomarkers of neurodegenerative diseases through speech analysis, was explored to identify the key factors in detecting PD from speech.

The project was completed as part of graduate coursework, supported by an international collaboration grant. It involved a partnership with a researcher and doctor from an Indian hospital, providing expert insights into Parkinson’s speech biomarkers.

---

## **Motivation**

Early detection of PD, especially in its early-onset form, is challenging due to subtle symptoms. Since ~90% of PD patients exhibit speech impairments, analyzing vocal characteristics becomes a promising, non-invasive method for early detection.

---

## **Techniques Used**

- Following the architecture proposed by Quan et al., the model uses a **two-stage CNN** to detect Parkinson’s Disease from speech:
  - **Time-Distributed 2D CNN**: Processes overlapping segments of log Mel-spectrograms to extract local spatial features while preserving temporal structure.
  - **1D CNN**: Captures temporal patterns such as jitter from the flattened 2D-CNN outputs.
  - **Final Layers**: Fully connected layers classify the extracted features to predict PD presence.
- **Mel-spectrograms** Used as image-like inputs, representing the mathematical features of sound
- **Librosa**: Utlized for audio processing and Mel spectrogram generation.
- **NeuroSpeech**:  Used for analyzing key speech features in PD patients, , focusing on phonation, articulation, prosody, and intelligibility.
- **Datasets**: Speech data collected in Italian, Telugu, and English

---
## **Project Workflow**

The overall workflow of the model, from speech input to Parkinson’s detection, is outlined below.

![Workflow](/images/PD_Detection_Workflow.svg)


------

## **Dataset and Processing**

- **Italian Dataset**: 394 HC samples and 437 PD samples from 65 participants.
- **Telugu Dataset**: 24 samples from 8 participants under varied noise conditions (created by the class).
- **English Dataset**: KCL Hospital phone-based recordings with detailed PD annotations.

Example of a Mel spectrogram generated from raw speech data: 
Left: Heatmap representation, Right: Frequency matrix

![Mel_Spectrogram](/images/Mel_spectrogram.png)


------

## **Tools & Libraries**

- Python
- TensorFlow / Keras
- Librosa
- NeuroSpeech
- Matplotlib / Seaborn (for visualization)

---

## **Results**

- Achieved **~98% validation accuracy** on Italian speech samples using improved preprocessing (2,000-frame spectrogram segments).
- Found **low-frequency spectrogram features** to be most indicative of PD.
- Cross-language testing revealed poor generalizability, highlighting the need for **language-specific models** when applying deep learning.

---

## **Challenges & Insights**

- **CNNs**, while powerful, suffer from a lack of interpretability, which is a significant concern in clinical settings.
- **Cross-language models** struggle without balanced training data, limiting their effectiveness.
- Future improvements include:
  - Expanding training sets for multilingual support
  - Exploring more interpretable machine learning algorithms like trees or building tools like NeuroSpeech, which directly extracts key speech features (such as articulation rate, pitch variability, and speech clarity) from audio and compares them against a database of healthy control (HC) and PD patient data to determine whether they fall within a normal or abnormal range.
---

## **Extras/ Resources**

- Read full project report here - [PDF](/Parkinsons_Approach_Report.pdf)
- Exploratory notebooks for Librosa audio processing - [Notebook](/Librosa_Feature_Extraction.pdf) 
---

## **References**

- [Quan et al., 2022: *End-to-End Deep Learning for PD Speech Detection*](https://www.sciencedirect.com/science/article/abs/pii/S0208521622000341)
- [Dimauro & Girardi, 2019: *Italian Parkinson’s Voice and Speech Dataset*](https://ieee-dataport.org/open-access/italian-parkinsons-voice-and-speech)
- [Orozco-Arroyave et al., 2018: *NeuroSpeech Tool*](https://www.sciencedirect.com/science/article/pii/S105120041730146X)
- [Jaeger et al., 2019: *KCL English Dataset (MDVR-KCL)*](https://explore.openaire.eu/search/dataset?pid=10.5281%2Fzenodo.2867215)


---

## Takeaway

Deep learning shows promise in detecting early-onset Parkinson’s from speech, but challenges in interpretability and cross-language generalization remain. Future advancements should focus on multilingual datasets and more interpretable approaches.

>Code available upon request