# UQ-TFGCN: Understanding Human Activity with Uncertainty Measure for Novelty in Graph Convolutional Networks

[![Paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/your-paper-id-here)
![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/repo-name)
![Status](https://img.shields.io/badge/Status-Code%20Coming%20Soon-blue)

This repository contains the official implementation for our paper "Understanding Human Activity with Uncertainty Measure for Novelty in Graph Convolutional Networks" (submitted to [The International Journal of Robotics Research]). We propose a novel approach for human activity recognition with uncertainty quantification using Graph Convolutional Networks (GCNs), evaluated on the Bimanual Actions and IKEA ASM datasets.

## 📌 Overview
![Sample OOD](images/OOD.png) 
- Novel architecture combining GCNs with uncertainty quantification
- Experimental evaluation on two challenging datasets:
  - **Bimanual Actions Dataset**
  - **IKEA ASM Dataset**
- Comprehensive analysis of novelty detection in human activities
- Quantitative evaluation of uncertainty measures

## 📥 Dataset Preparation

### Required Datasets
1. **Bimanual Actions Dataset**  
   Download from: [Bimanual Actions Dataset Website](https://bimanual-actions.humanoids.kit.edu/)  
2. **IKEA ASM Dataset**  
   Download from: [IKEA ASM Dataset Website](https://ikeaasm.github.io/)
3. **Data Generation**  
   *Code will be released soon.*

## 📊 Preliminary Results
### Action Recognition and Segmentation Performance Metrics
| Methods          | Accuracy| Macro-Recall | F1@10 | F1@25 | F1@50|
|------------------|---------|--------------|-------|-------|------|
| HCN (Li et al., 2018) | 39.15 | 28.18 | - | - | - |
| ST-GCN (Yan et al., 2018) | 43.40 | 26.54 | - | - | - | 
| multiview + HCN (Ben-Shabat et al., 2021) | 64.25 | 46.33 | - | - | - |
| ST-GCN+TPP (Xing and Burschka, 2022b) | 68.92 | 25.63 | 66.92 | 59.66 | 41.33 |
| AGCN + TPP (Xing and Burschka, 2022b) | 70.53 | 27.79 | 76.32 | 69.85 | 52.14 |
| MGAF (Kim et al., 2021) | 72.40 | 49.10 | - | - | - |
| CTR-GCN+TPP (Xing and Burschka, 2022b) | 78.70 | 37.98 | 78.84 | 72.68 | 54.40 |
| PGCN (Xing and Burschka, 2022b) | 79.35 | 38.29 | 81.53 | 76.28 | 58.07 |
| PIFLa (Yan et al., 2023) | **84.60** | **62.00** | - | - | - |
| **TFGCN (ours)** | 80.39 | 39.77 | **83.99** | **80.04** | **68.00** |
| **UQ-TFGCN (ours)** | 79.99 | 39.72 | 82.11 | 76.92 | 64.81 |

### OOD Detection Performance Metrics
| Methods          | AUROC^1 | AUPRC^1 | AUROC^2 | AUPRC^2 |
|------------------|---------|---------|---------|---------|
| MC-dropout | 99.95 ± 0.02 | 99.89 ± 0.02 | 78.00 ± 0.09 | 81.38 ± 0.08 |
| Ensemble | 99.81 ± 0.22 | 99.68 ± 0.33 | 86.29 ± 2.61 | 88.76 ± 2.17 |
| DUQ | 83.58 ± 3.98 | 80.96 ± 5.56 | 52.86 ± 7.43 | 57.00 ± 8.98 |
| SNGP        | 93.16 ± 3.44 | 84.67 ± 7.91 | 79.17 ± 1.89 | 78.03 ± 1.55 |
| **UQ-TFGCN** | 99.39 ± 0.97 | 99.13 ± 1.00 | 90.19 ± 0.92 | 92.07 ± 0.93 |

**Notes** 
- ^1 IKEA ASM is OOD
- ^2 Noisy Bimacs is OOD

### Visualization
#### Activity Recognition Samples and Uncertainty Gray Scale
![Sample Recognition](images/Bimacts.png) 

## 🛠 Installation & Usage
*Code will be released soon.*

Please cite:
```bibtex
  @article{xing2024understanding,
    title={Understanding human activity with uncertainty measure for novelty in graph convolutional networks},
    author={Xing, Hao and Burschka, Darius},
    journal={The International Journal of Robotics Research},
    pages={02783649241287800},
    year={2024},
    publisher={SAGE Publications Sage UK: London, England}
  }
```
Dataset
```bibtex
   @inproceedings{mateusz2018bimanual,
      title={Bimanual Actions Dataset},
      author={Mateusz, S. and colleagues},
      booktitle={IEEE Conference on Computer Vision and Pattern Recognition},
      year={2018}
    }

  @inproceedings{ikeaasm2020,
    title={IKEA ASM Dataset},
    author={Damen, D. and colleagues},
    booktitle={European Conference on Computer Vision},
    year={2020}

  }
```
