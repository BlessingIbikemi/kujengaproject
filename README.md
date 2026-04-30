# Do African-Built AI Models Actually Work Better on African Languages?

Testing AfroXLMR and AfriBERTa against a general multilingual model using real Nigerian Twitter sentiment data.

## The Question

Over 100 million Nigerians speak Yoruba, Igbo or Hausa. But most AI models were never built with these languages in mind. Researchers have created African-specific models like AfroXLMR and AfriBERTa to fix this gap.

**But do they actually work better?**

This project uses sentiment analysis data from AfriSenti and statistical t-tests to find out.

## The Models

- **XLM-RoBERTa** — General multilingual model (100 languages)
- **AfriBERTa** — African-specific, smaller model
- **AfroXLMR** — African-specific, larger model

## The Data

AfriSenti Twitter sentiment dataset:
- 99 tweets per language (Yoruba, Igbo, Hausa)
- Balanced across positive, negative, neutral labels
- Source: `shmuhammad/AfriSenti-twitter-sentiment` (HuggingFace)

## Key Findings

1. ✅ African-specific models **significantly outperform** general models (p < 0.05)
2. ✅ Even the smaller African model beats the general model
3. ❌ No significant difference between the two African models — size doesn't matter, training data does

## Files

- `notebook_final.ipynb` — Main analysis notebook
- `afrisenti_nigeria.xlsx` — Dataset (Yoruba, Igbo, Hausa tweets)
- `README.md` — This file
- `model_predictions.xlsx` — Results

## How to Run

1. Clone this repo
2. Install dependencies: `pip install transformers datasets scipy matplotlib seaborn pandas openpyxl torch`
3. Open `notebook_final.ipynb` in Jupyter or Google Colab
4. Run all cells top to bottom

## Built With

- Python 3.10
- HuggingFace Transformers
- AfriSenti dataset
- Statistical t-tests (scipy)

---

*Adetokunbo Blessing — 2026*
