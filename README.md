# Sentiment Analysis Project

This project focuses on sentiment analysis using two different techniques:

- **Unsupervised approach**: Learns sentiment patterns from raw text data without using labeled sentiment.
- **Discriminative approach**: Uses labeled data to directly classify the sentiment of a given text.

The dataset is divided into three parts:

- `train.csv`: Contains `sentiment`, `text`, and `data_id` columns for training.
- `valid.csv`: Similar format used for validation.
- `test.csv`: Contains `text` and `data_id`, where we need to predict and fill two new columns:
  - `out_label_model_1`: Predictions from the **unsupervised model**.
  - `out_label_model_2`: Predictions from the **discriminative model**.

Both models are trained and evaluated on the training/validation data, then saved to disk:

- Unsupervised model is saved to: `model/2400570/model_unsup`
- Discriminative model is saved to: `model/2400570/model_dis`

Once the models are trained and saved, they are automatically used during testing to generate predictions for the test set — **no need to retrain**. The `test.csv` file is then updated with predicted sentiment labels from both approaches.


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
3. Once saved, the trained models will automatically be used during the testing phase, retraining is not necessary unless the models are deleted.
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

