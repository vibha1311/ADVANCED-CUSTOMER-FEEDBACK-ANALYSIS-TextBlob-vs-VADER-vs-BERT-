# Advanced Customer Feedback Analysis (TextBlob vs VADER vs BERT)

## Project Overview

This project performs **advanced sentiment analysis** on customer feedback to extract insights from reviews and help businesses improve products, services, and customer experience. The project compares the performance of **TextBlob**, **VADER**, and **BERT (RoBERTa-base)** models on a mobile phone review dataset (`redmi6.csv`).

---

## Objective

- Classify customer reviews as **Positive**, **Negative**, or **Neutral**.  
- Compare outputs across multiple sentiment analysis models.  
- Visualize trends, patterns, and word frequency to generate actionable business insights.  

---

## Why This Project?

Customer reviews provide valuable feedback, but manually analyzing them is impractical. Automating sentiment analysis allows businesses to:

- Quickly measure **overall customer satisfaction**.  
- Identify **common issues or areas for improvement**.  
- Make **data-driven decisions** to enhance the customer experience.

---

## Models Used

1. **TextBlob**  
   - Lexical / Pattern-Based sentiment analysis using polarity scores.  
   - **Advantage:** Simple, interpretable.  
   - **Limitation:** Struggles with context and sarcasm.  

2. **VADER (Valence Aware Dictionary and sEntiment Reasoner)**  
   - Dictionary / Rule-Based optimized for social media and short text.  
   - **Advantage:** Good for short and informal text; decisive polarity.  
   - **Limitation:** May misclassify complex or domain-specific sentences.  

3. **BERT (RoBERTa – `cardiffnlp/twitter-roberta-base-sentiment-latest`)**  
   - Transformer-based deep learning model with contextual understanding.  
   - **Advantage:** Highly accurate for nuanced text.  
   - **Limitation:** Computationally heavy; slower than rule-based models.

---

## Advantages

- Automates sentiment classification for large datasets.  
- Compares multiple models to understand reliability and sensitivity.  
- Visualizes sentiment distribution via bar charts, pie charts, and word clouds.  
- Can be extended for **real-time feedback analysis**.  

---

## Limitations / Disadvantages

- BERT requires **GPU for faster performance**.  
- Rule-based models (TextBlob, VADER) may misclassify sarcasm or nuanced reviews.  
- Model accuracy depends on **data quality and preprocessing**.  
- Domain-specific vocabulary may need **custom lexicons** for better performance.

---

## Project Results: Sentiment Analysis Comparison

The sentiment analysis results show notable differences among the three models:

1. **VADER**  
   - Highest number of **Positive** predictions, followed by **Negative**, fewest **Neutral**.  
   - Optimized for social media text, tends to produce decisive scores.  

2. **BERT (RoBERTa-based)**  
   - High Positive counts with a **more balanced distribution** of Negative and Neutral.  
   - Understands context better, leading to nuanced predictions.  

3. **TextBlob**  
   - Prefers **Neutral** classification, less aggressive in assigning polarity.  

### Model Comparison Summary

| Model     | Classification Approach        | Key Observation                                                                 |
|-----------|-------------------------------|-------------------------------------------------------------------------------|
| **VADER** | Dictionary/Rule-Based         | Most decisive (highest Positive & Negative, lowest Neutral).                  |
| **BERT**  | Transformer-Based (RoBERTa)  | Strong performance with balanced distribution; understands context.            |
| **TextBlob** | Lexical/Pattern-Based       | Least sensitive, resulting in highest Neutral counts.                          |

---

### Visual Summary

- **Bar Chart:** Compares sentiment counts across all three models.  
- **Pie Charts:** Show sentiment proportion per model.  
- **Word Clouds:** Highlight frequent words in Positive and Negative reviews (BERT).  

---

### Single Sentence Analysis Example

The notebook includes an interactive function to test **any sentence** against all three models:

- **Example Sentence:** `"I love this product!"`  
- All three models agree on clear sentiment, demonstrating consensus for unambiguous sentences.

---

## How to Run

1. Clone the repository:
```bash
git clone <your-repo-url>
cd <repo-folder>

