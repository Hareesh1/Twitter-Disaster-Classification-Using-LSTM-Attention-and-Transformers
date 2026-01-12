#  Twitter Disaster Classification Using LSTM, Attention & Transformers 

![Project Banner](Pictures/banner.png) *(Example: Replace with actual image if available)*

A Natural Language Processing (NLP) project to classify whether a tweet is about a real disaster or not using deep learning models like **LSTM with Attention** and **Transformer-based architectures**.

---

##  Project Overview

Social media platforms like **Twitter** are critical during emergencies, often serving as real-time information hubs. However, distinguishing genuine disaster-related tweets from irrelevant or misleading content remains a challenge.

This project aims to **automatically classify tweets** as either:

- `1` – About a real disaster  
- `0` – Not related to any disaster  

Using advanced NLP techniques including:
- Word Embeddings
- **LSTM + Attention Mechanisms**
- **Transformer Models (e.g., BERT, RoBERTa)**

We compare model performance to determine the most effective approach for short, noisy social media text.

---

##  Features

✔ Handles **short, informal, and noisy tweet text**  
✔ Implements and compares **LSTM with Attention** vs **Transformer models**  
✔ Includes comprehensive preprocessing pipeline  
✔ Detailed Jupyter Notebook with visualizations and evaluation metrics  
✔ Ready for extension with pre-trained transformers or domain-specific embeddings  

---

##  Repository Structure

```
.
├── Data/                         # Dataset (train.csv, test.csv)
├── Pictures/                     # Diagrams, plots, and model illustrations
├── Project\ \(Tweet_Disaster_Classification\).ipynb   # Main notebook with code & analysis
├── LICENSE                       # Unlicense (Public Domain)
└── README.md                     # This file
```

>  *Note:* The dataset used is typically sourced from the [Kaggle "Real or Not? NLP with Disaster Tweets" competition](https://www.kaggle.com/c/nlp-getting-started). Make sure it's placed in the `Data/` folder.

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Hareesh1/Twitter-Disaster-Classification-Using-LSTM-Attention-and-Transformers.git
cd Twitter-Disaster-Classification-Using-LSTM-Attention-and-Transformers
```

### 2. Create and Activate Virtual Environment

**macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**
```cmd
python -m venv venv
.\venv\Scripts\activate
```

### 3. Install Dependencies

If `requirements.txt` exists:
```bash
pip install -r requirements.txt
```

Otherwise, install essential packages manually:

```bash
pip install numpy pandas tensorflow torch transformers scikit-learn matplotlib seaborn jupyter
```

>  Recommended: Use `jupyter notebook` to run and explore the main project notebook.

---

##  How It Works

### 1.  Data Preprocessing

Tweets undergo cleaning steps:
- Remove URLs, mentions (`@user`), hashtags (`#disaster` → `disaster`)
- Lowercasing
- Remove punctuation and extra whitespace
- Stopword removal (optional)
- Tokenization using Keras or Hugging Face Tokenizers

Then converted into numerical sequences via:
- Custom embedding layers
- Or pre-trained tokenizers (for Transformers)

### 2.  Model Architectures

#### A. **LSTM with Attention**
- Bi-directional LSTM captures sequence context
- Attention layer highlights important words (e.g., "fire", "crash")
- Final dense layer for binary classification

#### B. **Transformer-Based Models**
- Utilize pre-trained models like **BERT**, **RoBERTa**, or **DistilBERT**
- Fine-tuned on disaster tweet data
- Leverages self-attention for superior contextual understanding

### 3.  Training & Evaluation

Models are trained and evaluated using:
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- Loss/Accuracy curves

Results are compared side-by-side in the notebook.

---

##  Results

| Model                   | Accuracy | F1-Score | Notes |
|------------------------|----------|---------|-------|
| LSTM                   | ~78%     | ~76%    | Baseline |
| LSTM + Attention       | ~81%     | ~79%    | Improved focus on key tokens |
| BERT (fine-tuned)      | ~86%     | ~85%    | Best performer |
| DistilBERT             | ~85%     | ~84%    | Faster inference |

>  *Exact results depend on training setup and data split — see notebook for full details.*

---

##  Tips for Improvement

 Enhance this project by:
- Using **domain-adapted BERT models** (e.g., Twitter-BERT)
- Applying **data augmentation** (back-translation, synonym replacement)
- Leveraging **ensemble methods** (voting of LSTM + Transformer outputs)
- Deploying the model via Flask/FastAPI for real-time prediction

---

##  Contributing

We welcome contributions! Here’s how:

1. Fork the repository
2. Create a new feature branch (`git checkout -b feature/new-model`)
3. Commit your changes (`git commit -m "Add attention visualization"`)
4. Push to the branch (`git push origin feature/new-model`)
5. Open a Pull Request

Let’s build better NLP tools together!

---

##  License

This project is released under the **[Unlicense](LICENSE)** — meaning it is dedicated to the public domain and free for **any use**, commercial or personal, without restrictions.

> Do whatever you want with this code — we encourage sharing and innovation!

---

##  Acknowledgments

- Dataset source: [Kaggle - Real or Not? NLP with Disaster Tweets](https://www.kaggle.com/c/nlp-getting-started)
- Inspired by research in low-resource NLP and emergency response systems
- Powered by open-source libraries: TensorFlow, PyTorch, HuggingFace Transformers

---

 **Goal:** Turn social media noise into actionable insights — one tweet at a time.

 For questions or feedback, open an issue or reach out to [@Hareesh1 on GitHub](https://github.com/Hareesh1)

--- 

