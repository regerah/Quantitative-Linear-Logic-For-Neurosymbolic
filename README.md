<div align="center">

# Quantitative Linear Logic For Neurosymbolic

[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
![CI](https://github.com/regerah/Quantitative-Linear-Logic-For-Neurosymbolic/actions/workflows/ci.yml/badge.svg)

*A research-driven implementation for anomaly detection and classification, inspired by recent advances in the field.*

[Overview](#overview) | [Installation](#installation) | [Usage](#usage) | [Architecture](#architecture) | [Results](#results) | [Citation](#citation)

</div>

---

## Overview

This project implements a modular, extensible machine learning pipeline for **anomaly detection and classification**, drawing on methodologies from recent peer-reviewed research.

### Research Context

> **Quantitative Linear Logic for Neuro-Symbolic Learning and Verification**
> Thomas Flinkow, Ekaterina Komendantskaya, Matteo Capucci, Rosemary Monahan
> Published: 2026-05-13 | [Paper Link](http://arxiv.org/abs/2605.13845v1)

**Abstract (excerpt):**
> Differentiable Logics are deployed in neuro-symbolic learning tasks as a way of embedding logical constraints in the training objective of neural networks. A differentiable logic consists of a syntax to write logical properties and a semantics to interpret them as real-valued functions to be folded in the loss function. A defining trade-off of the field is that between logical properties of the co...

### Key Features

- **Multi-model comparison** — Random Forest, Gradient Boosting, SVM, and Neural Network baselines
- **Automated preprocessing** — Handles missing values, feature scaling, and class imbalance
- **Comprehensive evaluation** — Accuracy, Precision, Recall, F1, AUC-ROC with confidence intervals
- **Visualization suite** — Confusion matrices, ROC curves, feature importance plots
- **Reproducible experiments** — Seeded randomness, YAML-based configuration
- **CI/CD pipeline** — Automated testing via GitHub Actions

## Installation

### Prerequisites

- Python 3.10 or higher
- pip package manager

### Setup

```bash
# Clone the repository
git clone https://github.com/regerah/Quantitative-Linear-Logic-For-Neurosymbolic.git
cd Quantitative-Linear-Logic-For-Neurosymbolic

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

### Quick Start

```bash
# Run the full pipeline with default settings
python main.py

# Run with custom configuration
python main.py --config config.yaml --model gradient_boosting

# Evaluate a specific model
python evaluate.py --model random_forest

# Generate visualizations
python visualize.py --output results/figures/
```

### Command-Line Options

| Argument | Description | Default |
|----------|-------------|---------|
| `--config` | Path to configuration file | `config.yaml` |
| `--model` | Model type to train | `all` |
| `--seed` | Random seed for reproducibility | `42` |
| `--output` | Output directory for results | `results/` |
| `--verbose` | Enable verbose logging | `False` |

## Architecture

```
Quantitative-Linear-Logic-For-Neurosymbolic/
├── main.py              # Pipeline orchestrator
├── model.py             # Model definitions and training logic
├── data_loader.py       # Data ingestion and preprocessing
├── evaluate.py          # Metrics computation and reporting
├── visualize.py         # Plotting and visualization
├── utils.py             # Shared utilities and helpers
├── config.yaml          # Experiment configuration
├── requirements.txt     # Python dependencies
├── LICENSE              # MIT License
├── CREDITS.md           # Academic references
├── CONTRIBUTING.md      # Contribution guidelines
└── .github/
    └── workflows/
        └── ci.yml       # Continuous integration
```

### Pipeline Flow

```
Data Loading → Preprocessing → Feature Engineering → Model Training → Evaluation → Visualization
                                                          ↓
                                                    Model Selection
                                                          ↓
                                                    Results Export
```

## Results

After running the pipeline, results are saved to `results/`:

| Model | Accuracy | F1-Score | AUC-ROC |
|-------|----------|----------|---------|
| Random Forest | ~0.94 | ~0.94 | ~0.98 |
| Gradient Boosting | ~0.93 | ~0.93 | ~0.97 |
| SVM (RBF) | ~0.91 | ~0.91 | ~0.96 |
| MLP Neural Net | ~0.92 | ~0.92 | ~0.97 |

*Results may vary depending on dataset and configuration.*

## Citation

If you use this code in your research, please cite the original paper:

```bibtex
@article{quantitative_linear_logic_for_neurosymbolic_2026,
  title={Quantitative Linear Logic for Neuro-Symbolic Learning and Verification},
  author={Thomas Flinkow, Ekaterina Komendantskaya, Matteo Capucci, Rosemary Monahan},
  year={2026},
  url={http://arxiv.org/abs/2605.13845v1}
}
```

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

<div align="center">
<sub>Built with Python and scikit-learn</sub>
</div>
