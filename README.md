# ⚖️ CyberNyaya: Vernacular Cyber Harassment Detection & BNS Legal Action Engine

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB.svg)](https://reactjs.org/)
[![PyTorch](https://img.shields.io/badge/Deep%20Learning-PyTorch-EE4C2C.svg)](https://pytorch.org/)
[![BNS](https://img.shields.io/badge/Legal%20Framework-Bharatiya%20Nyaya%20Sanhita%20(BNS)-orange.svg)]()

**CyberNyaya** is an AI-powered cyber threat intelligence and legal redressal framework tailored for vernacular Indian online discourse (Hinglish / Romanized Hindi + English code-switching). It classifies digital hostility into stratified threat levels and probabilistically maps detected offenses to relevant sections of the **Bharatiya Nyaya Sanhita (BNS)**, automatically drafting formal legal complaints for cybercrime reporting.

---

## 🌟 Key Features

- **Vernacular Hinglish Normalization**: Advanced NLP preprocessing with deterministic Hinglish slang mapping, handling code-switching, transliteration, and colloquial abuse.
- **Dual-Model Hybrid ML Engine**:
  - **PyTorch Multi-Layer Perceptron (MLP)**: Non-linear deep feature extraction for threat severity stratification (*Low*, *Medium*, *High*).
  - **Multinomial Naive Bayes**: Probabilistic classifier mapping vocabulary distributions to specific Bharatiya Nyaya Sanhita (BNS) penal sections.
- **Automated Legal Redressal**: Generates structured, legally sound formal complaints and FIR drafts referencing relevant BNS sections (e.g., Section 351 Criminal Intimidation, Section 352 Intentional Insult).
- **Modern Interactive Dashboard**: High-performance React (Vite) interface with live threat scoring, visual breakdown metrics, and instant draft generation.
- **RESTful API**: Fast and decoupled FastAPI backend with modular endpoints.

---

## 🏗️ System Architecture

```text
User Input (Hinglish/English)
          │
          ▼
   [NLP Preprocessor]
 (Normalization & Vernacular Slang Mapping)
          │
          ▼
   [TF-IDF Vectorizer]
     ┌────┴───────────────────────────┐
     ▼                                ▼
[PyTorch MLP Engine]       [Multinomial Naive Bayes]
(Threat Level: Low/Med/High)   (BNS Legal Section Mapping)
     └────┬───────────────────────────┘
          ▼
  [FastAPI Backend]
          │
          ▼
[React UI & Automated Legal Draft Generator]
```

---

## 📁 Repository Structure

```text
├── backend/                  # FastAPI application & ML training scripts
│   ├── main.py               # REST API endpoints & inference handling
│   ├── train_models_v2.py    # Model training script
│   └── generate_realistic_cm.py
├── frontend/                 # Modern React (Vite) User Interface
│   ├── src/                  # React components and styling
│   ├── public/               # Public assets and icons
│   └── package.json
├── data/                     # Training datasets
│   └── v2_training_dataset.csv
├── models/                   # Serialized ML models & weights
│   ├── bns_nb_model.pkl      # Naive Bayes legal classifier
│   ├── threat_mlp_model.pt   # PyTorch MLP threat severity weights
│   └── tfidf_vectorizer.pkl  # Trained TF-IDF vectorizer
├── preprocessing.py          # Hinglish slang dictionary & normalization pipeline
├── predict.py                # Standalone inference helper
├── cybernyaya_theory.md      # Detailed academic/theoretical whitepaper
├── requirements.txt          # Python dependencies
└── run_all_tests.py          # Unified test verification suite
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Node.js 18+ & npm
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Backend Setup

```bash
# Optional: Create and activate a virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start FastAPI server
uvicorn backend.main:app --reload --port 8000
```
API Documentation will be accessible at: `http://localhost:8000/docs`

### 3. Frontend Setup

In a new terminal window:

```bash
cd frontend
npm install
npm run dev
```
Open `http://localhost:5173` in your browser.

---

## 🧪 Testing

Run the automated test suite to verify preprocessing, inference, and API endpoints:

```bash
python run_all_tests.py
```

---

## 📜 Legal & Theoretical Framework

For an in-depth academic study of the code-switching NLP architecture and legal mapping algorithms under the Bharatiya Nyaya Sanhita, refer to [cybernyaya_theory.md](cybernyaya_theory.md).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.
