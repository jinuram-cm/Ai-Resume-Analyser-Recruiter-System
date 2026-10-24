# AI Resume Analyzer & Recruiter System

An NLP-based tool that screens resumes against a job description and ranks candidates by how well they match.

## About the project

Recruiters receive many resumes for a single role, and screening them by hand is slow. This project uses Natural Language Processing (NLP) to compare each resume with the job description, calculate a similarity score, and rank candidates so the best matches can be reviewed first.

It can also help job seekers see how closely their resume matches a role.

## How it works

1. Load a resume (PDF or text)
2. Enter the job description
3. Clean and preprocess the text
4. Convert the text to vectors using TF-IDF
5. Calculate the similarity score (cosine similarity)
6. Rank candidates by score and display the results

## Tech stack

- Python
- [pandas, NumPy]
- [scikit-learn, NLTK or spaCy]
- [PDF library, for example PyPDF2 or pdfplumber]
- Jupyter Notebook

## Dataset

This project uses `jobs_dataset_with_features.csv` from the **EXAI-ResumeIntel datasets** by Mithin Sagar S (Vellore Institute of Technology), released under the MIT license.

- Source: [mithinsagar/exai-resumeintel-data on Hugging Face](https://huggingface.co/datasets/mithinsagar/exai-resumeintel-data)
- Contents: over 1 million job postings, with a `Role` column and a `Features` column of extracted skill text
- Size: about 638 MB

The file is not included in this repository because of its size. To download it:

```bash
pip install huggingface_hub
hf download mithinsagar/exai-resumeintel-data --repo-type dataset --local-dir data/raw
```

Then load it in the notebook, for example:

```python
import pandas as pd
df = pd.read_csv("data/raw/jobs_dataset_with_features.csv")
```

## How to run

1. Clone the repository:
   ```
   git clone https://github.com/jinuram-cm/Ai-Resume-Analyser-Recruiter-System.git
   ```
2. Install the requirements:
   ```
   pip install -r requirements.txt
   ```
3. Download the dataset (see the Dataset section above).
4. Open the notebook:
   ```
   jupyter notebook
   ```
5. Run all cells.

## Future improvements

- [A web interface for uploading resumes]
- [Better skill extraction]
- [Support for more file formats]

## Acknowledgements

Dataset by Mithin Sagar S, [EXAI-ResumeIntel](https://github.com/mithinsagar/EXAI-ResumeIntel), MIT license.

## Author

Jinu Ram C M - [LinkedIn](https://www.linkedin.com/in/jinu-ram-c-m-535876434/)
