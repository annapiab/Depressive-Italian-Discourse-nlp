# Modeling Depressive Patterns in Italian Discourse: insights from Natural Language Processing
by Annapia Borraccino, M.A (The Graduate Center, CUNY - New York, NY)

## 📘 Overview

This project investigates how depression manifests in the spontaneous speech of Italian speakers. Using transcriptions from the **Androids Corpus** (Tao et al., 2023), it combines psychological theory, linguistic analysis, and deep learning to identify linguistic markers associated with depression.

## 🧠 Motivation

Despite growing attention to mental health, depression remains stigmatized in many cultures, including Italy. Given that depression often manifests in subtle language patterns, this study explores how **Natural Language Processing (NLP)** can be used to detect depressive symptoms from textual data, offering a non-invasive tool for mental health monitoring.

## 🔍 Research Questions

1. **Which emotional and cognitive linguistic features distinguish depressed from non-depressed individuals?**  
2. **What linguistic signals do deep learning models rely on—and how do these align with psychological theories of depression?**

## 📂 Dataset

- **Source**: Tao et al. (2023) – *The Androids Corpus: A New Publicly Available Benchmark for Speech Based Depression Detection*
- **Samples**: 115 Italian interview transcripts (63 depressed, 52 control)
- **Tasks**: Interview Task (spontaneous speech only)

## 🛠 Methods

### 🔧 Feature-Based Modeling
- **Lexicon**: [ELIta](https://github.com/edipalm/EliTa) for emotional features
- **Linguistic Features**: pronouns, verb tense, negation, sentence complexity via [Stanza](https://stanfordnlp.github.io/stanza/)
- **Models**: Logistic Regression and SVM (baseline)
- **Accuracy**: **84%**, F1 (depressed): **0.87**

### 🤖 Transformer Modeling
- **Model**: Fine-tuned [BERTino](https://huggingface.co/Musixmatch/umberto-commoncrawl-cased-v1) (Italian BERT variant)
- **Tokenization**: WordPiece + [CLS]
- **Explainability**: [BERTViz](https://github.com/jessevig/bertviz) for attention insights
- **Accuracy**: **92%**, **Perfect recall** for depressed class

## 📈 Results Summary

| Model     | Accuracy | F1 (Depressed) | Notable Features |
|-----------|----------|----------------|------------------|
| SVM       | 84%      | 0.87           | Joy, past tense, negation, 1st-person markers |
| BERTino   | 92%      | 1.00           | Self-focus, negation, family/health/time themes |

## 🧩 Key Contributions

- Cross-linguistic validation of depression markers in **Italian**
- Integration of **psycholinguistic theory** with **explainable AI**
- Demonstrated utility of **text-only** models in mental health screening

