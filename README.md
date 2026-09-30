# 🎸 Classic Rock Voice Cloning & Stem Separation Pipeline

An end-to-end, reproducible Python audio machine learning pipeline built in Google Colab. This project demonstrates vocal stem isolation, zero-shot generative voice synthesis, and Mel-spectrogram spectral analysis using classic rock audio—specifically Brad Delp’s iconic lead vocal from Boston’s *"More Than a Feeling"*.

> **Note on Scope:** This repository focuses strictly on the core Machine Learning mechanics (audio ingestion, source separation, flow-matching synthesis, and DSP analysis). Production cloud orchestration (AWS S3/SQS, FastAPI microservices, and serverless GPU scaling) is intentionally excluded to keep the notebook self-contained and reproducible.

---

## 🌟 Key Features

* **Source Separation:** Utilizes **HTDemucs** to separate music tracks into isolated 24-bit vocal stems, stripping out heavy guitars, drums, and room reverb.
* **Zero-Shot Voice Synthesis:** Leverages **F5-TTS** (Flow-Matching Transformer) to extract speaker timbre and condition generative voice cloning without requiring model retraining or fine-tuning.
* **Spectral Analysis & QA:** Integrates `librosa` and `matplotlib` to render side-by-side **Mel-spectrograms**, allowing visual inspection of harmonic alignment, formants, and sibilance.
* **Language Agnostic Prompting:** Demonstrates cross-lingual zero-shot cloning (synthesizing Spanish/English prompts using an English reference vocal stem).

---

## 🏗️ Architecture & Pipeline Stages
