# Self-Coded LLM Evaluated Results

## Overview
This Jupyter Notebook evaluates a self-coded tokenizer and prepares data for training a language model. It processes text from `the-verdict.txt`, tokenizes it using a custom tokenizer and `tiktoken`, and constructs a dataset for model training.

## Features
- Reads and preprocesses a text dataset
- Implements a simple tokenization method (`SimpleTokenizerV2`)
- Uses `tiktoken` for encoding text with GPT-2 tokenization
- Prepares dataset using a sliding window approach for GPT training
- Constructs a PyTorch `Dataset` and `DataLoader`

## Setup & Installation
To run the notebook, install the necessary dependencies:
```bash
pip install tiktoken torch
```

Alternatively, install from a `requirements.txt` file (if available):
```bash
pip install -r requirements.txt
```

## How to Use
1. Load your dataset by modifying the file path:
   ```python
   with open("/path/to/your/dataset.txt", "r", encoding="utf-8") as f:
       raw_text = f.read()
   ```
2. Modify tokenization rules in `SimpleTokenizerV2` to customize preprocessing.
3. Adjust dataset parameters like:
   ```python
   context_size = 4  # Modify to change the input sequence length
   stride = 128      # Adjust overlap between training samples
   ```
4. Use the `GPTDatasetV1` class to create a dataset for training.
5. Modify the `DataLoader` batch size as needed.

## Customization
- **Use a different dataset**: Replace `the-verdict.txt` with another text file.
- **Change tokenization strategy**: Adjust `SimpleTokenizerV2` or replace it with another tokenizer.
- **Modify training parameters**:
  - Change `context_size` to vary input sequence length.
  - Adjust `stride` to control dataset overlap.
  - Modify `batch_size` for training efficiency.
- **Integrate a model**: Replace the placeholder training logic with an actual GPT model training loop.

## Results & Evaluation
- The notebook provides encoded outputs and visualizes tokenization.
- You can add model evaluation metrics to assess different tokenization techniques.

## Contribution
Fork and modify this notebook to improve tokenization, dataset preparation, or training workflows. Contributions in optimizing tokenization, adding new models, or improving evaluation techniques are welcome!

for more changes understande the code
