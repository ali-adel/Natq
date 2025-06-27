# 🗣️ Natq: Arabic Text-to-Speech System

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Python](https://img.shields.io/badge/python-3.10+-blue.svg)

**Natq** (نطق) is an open-source Arabic Text-to-Speech (TTS) system developed as a graduation project at the Faculty of Computing and Artificial Intelligence, Helwan University. This system supports high-quality Arabic speech synthesis using modern deep learning models—built from scratch using public datasets and designed to handle diacritization and grapheme-to-phoneme (G2P) conversion for Arabic.

<p align="center">
  <img src="assets/natq_pipeline.png" alt="Pipeline" width="80%">
</p>

---

## 🌟 Highlights

- 🎙️ Arabic support with diacritics & phoneme-level control
- ⚙️ Models: FastPitch, FastSpeech2, Mixer-TTS, Spark-TTS, HiFi-GAN
- 🤖 End-to-end & modular pipelines
- 🔈 High-quality waveform synthesis
- 🚀 Deployment-ready with FastAPI & React
- 🗃️ Open datasets: ClArTTS & Arabic Speech Corpus

---

## 📜 Abstract

Arabic is a complex and low-resource language for TTS. Our project tackles the challenges of limited annotated speech corpora and the absence of diacritics, which are essential for correct pronunciation. We propose a modular Arabic TTS system using deep learning with:

- Transformer-based mel-spectrogram generators
- A state-of-the-art HiFi-GAN vocoder
- A novel LLM-based TTS model: Spark-TTS
- Integration of diacritization (CATT) and phoneme conversion (Nawar Halabi’s Phenomizer)

---

## 🧠 Model Architecture

<p align="center">
  <img src="assets/models_overview.png" alt="Models" width="80%">
</p>

### 🔧 Spectrogram Generators
- [FastPitch](https://arxiv.org/abs/2006.06873)
- [FastSpeech2](https://arxiv.org/abs/2006.04558)
- [Mixer-TTS](https://arxiv.org/abs/2306.12313)
- [Spark-TTS](https://arxiv.org/abs/2401.05930)

### 🌀 Vocoder
- [HiFi-GAN](https://arxiv.org/abs/2010.05646)

### 🔡 Preprocessing
- CATT for diacritization
- Nawar Halabi's G2P converter (Phenomizer)

---

## 🧪 Samples

| Model        | Sample 1 | Sample 2 |
|--------------|----------|----------|
| FastPitch    | 🔊 [Play](samples/fastpitch_1.wav) | 🔊 [Play](samples/fastpitch_2.wav) |
| Mixer-TTS    | 🔊 [Play](samples/mixer_1.wav)    | 🔊 [Play](samples/mixer_2.wav)    |
| Spark-TTS    | 🔊 [Play](samples/spark_1.wav)    | 🔊 [Play](samples/spark_2.wav)    |
| FastSpeech2  | 🔊 [Play](samples/fs2_1.wav)      | 🔊 [Play](samples/fs2_2.wav)      |

> 🎧 All models evaluated on both ClArTTS and Arabic Speech Corpus.

---

## 🚀 Deployment

You can deploy the TTS system locally using:

### Backend (FastAPI)
```bash
cd app
pip install -r requirements.txt
uvicorn main:app --reload

