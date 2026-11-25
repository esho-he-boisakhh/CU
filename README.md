# Phishing URL Detection using Deep Learning

This repository contains implementations and experiments for phishing URL detection using published deep learning approaches and a CharacterBERT-based classification model.

## Project Contents

### 1. `all_DL_models_for_comparison.ipynb`

Implementations and comparative evaluation of models from published research:

- Vinayakumar et al. — LSTM
- Saxe and Berlin — eXpose
- Wei et al. — Character-level CNN
- Phish-Armour — LSTM and GRU with lexical features
- Bu and Cho — Convolutional Autoencoder
- Alshehri et al. — Character-level CNN
- Huang et al. — PhishingNet
- Ozcan et al. — DNN–LSTM
- Akçam — PDRCNN / BiLSTM

### 2. `Final_Work1.ipynb`

CharacterBERT-based phishing URL classification.

CharacterBERT embeddings are used with a feature projection layer and recurrent classifiers. LSTM, BiLSTM, GRU, and BiGRU configurations are evaluated. LIME is also used for model interpretation.

**Best-performing configuration: BiGRU**

| Metric | Score |
|---|---:|
| Accuracy | **92.57%** |
| Precision | 90.99% |
| Recall | 94.36% |
| F1-score | 92.64% |

## Comparative Results

| Model | Reported accuracy | Reproduced result |
|---|---:|---:|
| Vinayakumar et al. (LSTM) | 99.96% | 86.3% |
| eXpose | Not checked | 90.6% |
| Wei et al. (Character CNN) | 99.98% | 64.2% |
| Phish-Armour (LSTM / GRU) | 90.5% / 98.5% | 75.5% / 68.3% |
| Bu and Cho (Autoencoder) | Not checked | 55% |
| Alshehri et al. (Character CNN) | 98.13% | 93.9% |
| PhishingNet | 97.9% | 90.8% |
| Ozcan et al. (DNN–LSTM) | Not checked | F1: 0.675 |
| PDRCNN | — | No saved outputs |

The CharacterBERT-based classifier achieved **92.57% accuracy** in its best recorded configuration.

## Dataset

The experiments use phishing URL data containing `url` and `status` fields, distinguishing legitimate URLs from phishing URLs. The dataset is not included in this repository.

## References

The model implementations are based on the research works identified in the comparison table. Refer to the original publications for their proposed architectures and methodologies.

## Disclaimer

This repository is intended for research and educational purposes. Model predictions should not be treated as a guarantee that a URL is safe or malicious.
