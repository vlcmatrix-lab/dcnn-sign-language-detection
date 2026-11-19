# Enhanced Model for Sign Language Detection with Deep CNN: Achieving Perfect Accuracy in Hand Gesture Recognition

[![DOI](https://img.shields.io/badge/DOI-10.1109%2FICIC63915.2024.11116573-blue)](https://doi.org/10.1109/ICIC63915.2024.11116573)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Abdul Rehman, Muhammad Zaman, Tanzila Kehkashan, Faheem Akbar, Muhammad Hamza, Raja Adil Riaz**

*2024 5th International Conference on Innovative Computing (ICIC), IEEE, 2024*

[Paper (IEEE Xplore)](https://ieeexplore.ieee.org/document/11116573) | [Author's accepted version (PDF)](paper/dcnn_sign_language_icic2024.pdf)

This repository accompanies the paper. It currently contains the paper and citation information only. See [Code availability](#code-availability).

## Summary

The paper presents DCNN v2, a deep convolutional neural network that classifies images of hand signs into the 26 letters of the American Sign Language (ASL) alphabet. Images are resized and normalized, and data augmentation (for example brightness, sharpness and zoom changes) is used to reduce overfitting. The network stacks convolutional layers with 64, 128, 256, 512 and 1024 filters, each followed by batch normalization and ReLU activation, then global average pooling, a dense layer with dropout, and a softmax output over the 26 classes. The model was built with TensorFlow and Keras and trained on Kaggle with two NVIDIA Tesla T4 GPUs.

The paper reports 100% accuracy, precision, recall and F1-score for DCNN v2 on the ASL dataset.

## Repository structure

```
dcnn-sign-language-detection/
├── paper/
│   └── dcnn_sign_language_icic2024.pdf   # author's accepted version
├── CITATION.cff
├── LICENSE
└── README.md
```

## Code availability

The code link given in the paper (`github.com/mani5100/Hand-Sign-Language-Detection`) is no longer available. The original training notebook will be added to this repository once it has been recovered. Installation and usage instructions will be added with it.

## Dataset

The paper uses the **American Hand Sign Detection** dataset from Kaggle: 26 classes (the letters A to Z of the ASL alphabet), with RGB images of 200x200 pixels.

- Official source: [Kaggle: American Hand Sign Detection](https://www.kaggle.com/datasets/konami9889/american-hand-sign-detection)

No data is included in this repository. Please download the dataset from the official source and follow its license terms.

## Results

All values below are reported in the paper.

**Training settings (Table I)**

| Dataset | Cross-validation | Epochs | Folds | Learning rate | Batch size | Optimizer | Seed | Image size |
|---|---|---|---|---|---|---|---|---|
| ASL | Stratified K-Fold | 15 | 8 | 0.001 | 32 | Adam | 42 | 200x200 |

**Comparison with other models (Table II, in %)**

| Model | Accuracy | Precision | Recall | F1-score |
|---|---|---|---|---|
| **DCNN v2 (proposed)** | **100** | **100** | **100** | **100** |
| CNN+RTS (baseline) | 98 | 96 | 97.1 | 96.4 |
| CNN | 90 | 98 | 98 | 98 |
| CNN | 96.3 | 96.8 | 97.3 | 96.2 |
| CNN | 92.9 | 93.2 | 93.6 | 93.1 |

The comparison models are cited in the paper.

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{rehman2024enhanced,
  author    = {Rehman, Abdul and Zaman, Muhammad and Kehkashan, Tanzila and Akbar, Faheem and Hamza, Muhammad and Riaz, Raja Adil},
  title     = {Enhanced Model for Sign Language Detection with Deep {CNN}: Achieving Perfect Accuracy in Hand Gesture Recognition},
  booktitle = {2024 5th International Conference on Innovative Computing (ICIC)},
  publisher = {IEEE},
  year      = {2024},
  doi       = {10.1109/ICIC63915.2024.11116573}
}
```

## Copyright notice

© 2024 IEEE. Personal use of this material is permitted. Permission from IEEE must be obtained for all other uses. The final version is published at DOI: [10.1109/ICIC63915.2024.11116573](https://doi.org/10.1109/ICIC63915.2024.11116573).

The PDF in `paper/` is the authors' accepted version, not the publisher's typeset version.

## License

The contents of this repository, other than the paper, are released under the [MIT License](LICENSE). The copyright notice above applies to the paper.
