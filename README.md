
# 🐦 Tweet Sentiment Classification

This project classifies tweets as **positive (1)** or **negative/neutral (0)** using both:
- ✅ XGBoost (baseline model)
- 🔥 BERT transformer (fine-tuned)

## 📊 Analysis Report

The project report summarizes the model architecture, data preprocessing, evaluation metrics, and deployment strategies.

📄 [View Project Report (PDF)](./tweet_report.pdf)


## 📁 Project Structure

```
.
├── app.py                  # Flask API
├── streamlit_app.py        # Streamlit UI
├── model/                  # Trained BERT model
├── requirements.txt
├── Dockerfile
├── analysis.py             # Model evaluation
├── data/                   # Raw and cleaned dataset
└── README.md
```

## 🚀 Features

- Preprocessing: stopword removal, lemmatization, emoji + hashtag cleanup
- Training pipeline for XGBoost and BERT
- Evaluation with classification report + accuracy
- Deployment using Flask API and Streamlit
- Docker support
- HuggingFace model upload-ready

## 📊 Evaluation

**XGBoost Classifier**
- Accuracy: 95.18%
- F1 (positive): 0.55

**BERT Model**
- Accuracy: 97.8%
- F1 (positive): 0.93

## 🧪 Example API Call

```bash
curl -X POST http://localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"text": "The stock market is crashing today!"}'
```

## 🐳 Docker

```bash
docker build -t tweet-flask-api .
docker run -p 5000:5000 tweet-flask-api
```

## 🧠 Streamlit

```bash
streamlit run streamlit_app.py
```

## 📦 Requirements

```bash
pip install -r requirements.txt
```

## 📝 Author

Garvit Kumbhat · [@garvit-kumbhat](https://github.com/garvit-kumbhat)
Dhruv Ruhela · [@RuhelaDhruv745](https://github.com/RuhelaDhruv745)

---

**This is a sentiment classification project built as an end-to-end ML pipeline with model training, analysis, and deployment.**
