# NLP Coursework 2026

## Repository Structure

The `BestModel` folder contains:
- The Jupyter notebook `BestModel` used to train the final model and generate predictions
- `dev.txt` — model predictions on the official development set
- `test.txt` — model predictions on the official test set
- `model/` — folder containing the saved model configuration and tokenizer

## Notebook Description

The Jupyter notebook is based on the baseline setup provided by the task organisers, [RoBERTa-base baseline model](https://colab.research.google.com/drive/1M5Qx-FVJYNqFdvpJgggIZaWk5SpGS1Nu?usp=sharing). 
From the **Preprocessing cell onward**, all code was written by the author as part 
of the proposed approach described in the report.

## Pretrained Model Weights

The pretrained model weights are too large to store in this repository.
Download them from Google Drive and place them inside the `BestModel/model/` folder:

[Download pretrained model weights](https://drive.google.com/file/d/14R4Mz-fd3e9kocsXY1XF72jCN6vQCCDE/view?usp=sharing)

## Results

| Split | File | F1 Score |
|---|---|---|
| Development set | `BestModel/dev.txt` | 0.5761 |
| Test set | `BestModel/test.txt` | TBD (leaderboard) |

## Model Configuration

| Parameter | Value |
|---|---|
| Base Model | RoBERTa-large |
| Number of Labels | 2 |
| Epochs | 5 |
| Learning Rate | 1e-5 |
| Weight Decay | 0.01 |
| Warmup Ratio | 0.1 |
| Max Sequence Length | 128 |
| Train Batch Size | 4 |
| Class Weight No PCL | 0.552 |
| Class Weight PCL | 5.274 |
| Random Seed | 42 |

## Requirements
```bash
pip install simpletransformers torch pandas scikit-learn
```
