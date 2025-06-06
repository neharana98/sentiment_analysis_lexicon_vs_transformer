# Sentiment and Emotion Analysis - Lexicon vs. Transformer

**Overview**:
With the surge in user-generated content, analysing sentiments and emotions from text has become a key task in NLP. Two popular approaches for this — Lexicon-based and Transformer-based models — each offering distinct advantages. This project explores both, comparing their effectiveness in extracting sentiment from social media-style text.

**Objective**:
To compare the performance of lexicon-based models with a transformer-based model (BERT) for sentiment and emotion analysis, particularly under structured and noisy text conditions.

**Dataset**:
Two fabricated datasets were created with GenAI.
1. Structured Text: formal, well-composed English comments that use standard grammar and vocabulary, are expressive using words rather than symbols or exaggeration, and avoid slang, emojis, or informal phrasing.
2. Noisy Text: composed of informal, unstructured text, mimicking user-generated content on social media. Contain abbreviations, phonetic spellings, or slang, and express sentiments and emotions with emojis, punctuation emphasis, and fragmented conversational phrases.

**Methodology**:

1. Three models for sentiment analysis:

| Model Type        | Model Name         | Characteristics                                               |
| ----------------- | ------------------ | ------------------------------------------------------------- |
| Lexicon-Based     | TextBlob           | Uses polarity scores from a predefined lexicon                |
| Lexicon-Based     | VADER              | Rule-based with valence scores, optimised for social text     |
| Transformer-Based | Twitter-RoBERTa    | Fine-tuned on Twitter data for robust sentiment understanding |

2. Two models for emotion analysis:

| Model Type        | Model Name          | Characteristics                                              |
| ----------------- | ------------------- | ------------------------------------------------------------ |
| Lexicon-Based     | NRC Emotion Lexicon | Tags words with 8 basic emotions                             |
| Transformer-Based | BERT GoEmotion      | Fine-tuned on GoEmotions dataset for 28 nuanced emotions     |

**Findings**:
On structured text, lexicon-based models (TextBlob and VADER) performed well, but on noisy text, the performance of lexicon-based models dropped significantly, while the transformer-based Twitter-RoBERTa showed a notable improvement in accuracy (80%). In emotion detection, the BERT GoEmotion model outperformed NRC both in structured and noisy contexts, capturing more nuanced emotions with higher alignment to sentiment tags (85% coherence between Twitter-RoBERTa and BERT GoEmotion).
