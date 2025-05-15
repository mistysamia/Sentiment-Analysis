# Sentiment Analysis Project

This project performs sentiment analysis using two approaches: an **unsupervised** method and a **discriminative** method. It includes model training, evaluation, and prediction, with the trained models saved for future testing.

---

## Dataset Structure

Located in the `data/20/` folder:

- `train.csv`: Contains `sentiment`, `text`, `data_id`
- `valid.csv`: Contains `sentiment`, `text`, `data_id`
- `test.csv`: Contains `text`, `data_id`, `out_label_model_1`, `out_label_model_2`

Predictions are required for:

- `out_label_model_1`: Using the unsupervised approach
- `out_label_model_2`: Using the discriminative approach

---

## Model Saving Paths

- Unsupervised model: `model/2400570/model_unsup`
- Discriminative model: `model/2400570/model_dis`

---

## Python Version and Dependencies

- **Python Version**: 3.11.11

### Required Libraries:

- `pandas==2.2.2`
- `numpy==1.26.4`
- `seaborn==0.13.2`
- `matplotlib==3.8.0`
- `tensorflow==2.17.1`
- `nltk==3.9.1`
- `scikit-learn==1.6.0`
- `spacy==3.7.5`
- `gensim==4.3.3`

### Installation:

```bash
pip install pandas==2.2.2 numpy==1.26.4 seaborn==0.13.2 matplotlib==3.8.0 tensorflow==2.17.1 nltk==3.9.1 scikit-learn==1.6.0 spacy==3.7.5 gensim==4.3.3
```

## Project Setup Instructions

1. Ensure **Python 3.11.11** is installed.
2. Install all required libraries listed above.
3. Create a project folder (e.g., `SentimentAnalysis/`)
4. Place the following inside the folder:
   - `data/` folder with dataset files
   - `model/` folder
   - `code.ipynb` file
5. Adjust file paths in the code to correctly point to the dataset and model save locations.

---

## Running the Code

1. Open and run `code.ipynb`.
2. Models will be trained and saved to their respective paths:
   - Unsupervised: `model/2400570/model_unsup`
   - Discriminative: `model/2400570/model_dis`
3. Once saved, the trained models will automatically be used during the testing phase — retraining is not necessary unless the models are deleted.
4. The `test.csv` file will be updated with the predicted sentiment labels:
   - `out_label_model_1`: from the unsupervised model
   - `out_label_model_2`: from the discriminative model

---

## Output

- Updated `test.csv` file with predictions from both models.
- Trained models saved in `model/2400570/` directory.

---

## Other Files

- `Presentation_sm23788.pdf`: Project presentation slides.
- `Report_sm23788.pdf`: A detailed report explaining:
  - Model performance
  - Evaluation metrics
  - Rationale for model selection
  - Comparisons with state-of-the-art (SOTA) techniques

