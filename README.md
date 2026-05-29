# Hallucination Detector

A machine learning project that detects when a language model is likely hallucinating, using token probability and self-consistency signals.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shlokbandiwar/hallucination-detector/blob/main/hallucination_detector.ipynb)

## What this project does
- Extracts token probability and self-consistency signals from GPT-2
- Trains a logistic regression classifier on 600 labeled examples from TruthfulQA
- Detects hallucinations with 58% accuracy
- Documents failure cases honestly — including hallucinations the detector misses and correct answers it wrongly flags

## Key finding
Token probability from GPT-2 reflects how common a phrase is on the internet, not whether it is factually correct. A conspiracy theory repeated millions of times online will always outscore an obscure correct fact. Any hallucination detector built on a weak base model inherits that model's blind spots.
