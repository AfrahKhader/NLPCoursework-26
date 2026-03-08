# NLP Coursework 2026

## Repository Structure

The `BestModel` folder contains:
- The Jupyter notebook used to train the final model and generate predictions
- `dev.txt` — model predictions on the official development set
- `test.txt` — model predictions on the official test set
- `model/` — folder containing the saved model configuration and tokenizer

## Notebook Description

The Jupyter notebook is based on the baseline setup provided in the coursework. 
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

## Requirements
```bash
pip install simpletransformers torch pandas scikit-learn
```

## Model Details

| Parameter | Value |
|---|---|
| Base Model | RoBERTa-large |
| Epochs | 5 |
| Learning Rate | 1e-5 |
| Max Sequence Length | 128 |
| Random Seed | 42 |
