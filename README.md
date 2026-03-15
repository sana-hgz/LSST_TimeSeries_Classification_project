# LSST_TimeSeries_Classification_project

Comparison of time series foundation models (MOMENT, Mantis) against supervised 
baselines (FCN, InceptionTime) on the LSST astronomical dataset from the UEA benchmark.

## Project Structure
- `LSST_Classification.ipynb` — main notebook (data, models, results)

## Models
- **FCN** — Fully Convolutional Network (baseline)
- **InceptionTime** — Inception-based deep learning baseline
- **MOMENT** — Foundation model (linear probing + full fine-tuning)
- **Mantis** — Contrastive foundation model (linear probing + fine-tuning)

## Results

| Model | Accuracy | Macro-F1 |
|---|---|---|
| FCN | 61.7% | 44.1% |
| InceptionTime | 47.4% | 29.0% |
| MOMENT – Linear Probe | 61.0% | 35.2% |
| MOMENT – Full Fine-tuning | **66.3%** | 46.4% |
| Mantis – Linear Probe | 60.4% | **50.4%** |
| Mantis – Fine-tuned | 62.0% | 47.7% |

## Requirements
```bash
pip install momentfm mantis-tsfm tslearn scikit-learn peft torch
```

## Usage
Open `LSST_Classification.ipynb` in Google Colab and run all cells.
