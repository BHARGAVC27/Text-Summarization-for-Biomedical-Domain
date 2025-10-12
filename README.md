# Text-Summarization-for-Biomedical-Domain


## Overview

This repository contains code developed for automating the summarization of biomedical research articles using natural language processing techniques. Both extractive and abstractive summarization methods are implemented and evaluated on the PubMed dataset.

## Repository Structure

- **abstractive_summarization.ipynb**: Notebook for fine-tuning and evaluating abstractive summarization models such as BioBART, BART, PEGASUS, and T5 on PubMed articles.
- **extractive_summarization.ipynb**: Notebook implementing extractive summarization algorithms (TextRank, LexRank) with evaluation.
- **requirements.txt**: Python dependencies required to run the notebooks.
- **README.md**: Project overview and instructions (this file).

## Setup Instructions

1. Clone this repository:   
```bash
git clone https://github.com/BHARGAVC27/Text-Summarization-for-Biomedical-Domain.git
cd Text-Summarization-for-Biomedical-Domain
```

2. Use a Python 3.8+ environment with Jupyter notebooks or Google Colab.
3. Install the required dependencies:
  ```
  pip install -r requirements.txt
  ```
or ignore (installation commands provided in notebooks)
4. The PubMed summarization dataset is automatically loaded within the notebooks via the Hugging Face `datasets` library.

## How to Run

### Abstractive Summarization Notebook

- Run `abstractive_summarization.ipynb` to fine-tune BioBART and compare pretrained abstractive models.
- GPU runtime is recommended for faster training and evaluation.
- Note: The fine-tuned model checkpoint is **NOT included** in this repository. Running this notebook will **start training the model from scratch**.
- Save any fine-tuned model checkpoint locally or to Google Drive to avoid retraining.

### Extractive Summarization Notebook

- Run `extractive_summarization.ipynb` to generate and evaluate extractive summaries using TextRank and LexRank.
- CPU runtime is sufficient for extractive summarization.
- The notebook preprocesses articles similarly to the abstractive pipeline for consistency.

## ROUGE Evaluation

Both notebooks use ROUGE-1, ROUGE-2, and ROUGE-L metrics to quantitatively assess the informativeness and fidelity of generated summaries compared to reference abstracts.

## Important Notes

- Ensure the runtime environment allows installing all dependencies and has access to download datasets from Hugging Face.
- Save fine-tuned models promptly to prevent data loss from runtime interruptions.

## Contact and Support

For any questions or issues regarding this project, please contact the project maintainer or Teaching Assistants assigned to this course.



