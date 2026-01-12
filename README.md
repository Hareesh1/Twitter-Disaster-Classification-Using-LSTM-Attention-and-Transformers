##Twitter Disaster Classification Using LSTM, Attention & Transformers 

Twitter Disaster Classification is a Natural Language Processing (NLP) project for classifying tweets related to disasters. The goal is to distinguish real disaster-related tweets from unrelated noise using advanced sequential models like LSTM with attention and Transformer-based architectures.

This repository implements and compares different deep learning techniques to capture linguistic context and classify tweets accurately.

Project Overview

Social media (especially Twitter) is widely used during emergencies to broadcast real-time information. Identifying tweets that genuinely relate to disasters helps first responders, analysts, and automated systems to act faster and filter irrelevant chatter.

This project explores:

Embedding Techniques – Word embeddings to represent tweet text

Sequential Modeling – Long Short-Term Memory (LSTM) networks

Attention Mechanisms – To focus on important parts of text

Transformer Models – For advanced contextual understanding

🧠 Features

✔ Handle noisy and short text (tweets)
✔ Compare performance of LSTM + Attention against Transformer-based models
✔ Detailed project notebook for experimentation

📁 Repository Contents
.
├── Data/                         # Dataset used for training/testing
├── Pictures/                     # Visualizations or illustrations
├── Project (Tweet_Disaster_Classification).ipynb   # Main notebook with implementation and results
├── LICENSE                       # Unlicense (public domain dedication)
└── README.md                     # This file

🛠️ Installation

Clone the repository

git clone https://github.com/Hareesh1/Twitter-Disaster-Classification-Using-LSTM-Attention-and-Transformers.git
cd Twitter-Disaster-Classification-Using-LSTM-Attention-and-Transformers


Create & activate a Python environment

python3 -m venv venv
source venv/bin/activate    # macOS/Linux
.\venv\Scripts\activate     # Windows


Install dependencies

pip install -r requirements.txt


If a requirements.txt file isn’t available, you may need common NLP/deep learning packages like:

numpy, pandas, tensorflow, keras, torch

transformers (optional for Transformers)

scikit-learn
You can install with:

pip install numpy pandas tensorflow transformers scikit-learn

💡 How It Works
1. Data Preprocessing

Tweets are cleaned (removing URLs, punctuation, stopwords)

Tokenization and embedding generation

2. Model Architectures

LSTM Model – Captures sequential dependencies

Attention Mechanism – Helps model focus on key tokens

Transformer Models – Capture contextual relations with self-attention

3. Training & Evaluation

Train on labeled dataset (disaster vs non-disaster)

Evaluate with metrics such as accuracy, precision, recall, F1

📊 Results

The training results can be visualized and compared within the Jupyter notebook. The comparative results show how each model performs on the disaster tweet classification task.

📌 Notes

You can extend the project with pre-trained Transformer models (like BERT or RoBERTa) for even stronger performance.

Consider data augmentation or domain-specific embeddings to handle noisy Twitter data.

❤️ Contributing

Contributions are welcome! You can:

Fork the repo

Create a feature branch

Commit your changes

Open a pull request

📜 License

This project is released under the Unlicense, meaning it’s dedicated to the public domain and free for any use.
