# Spam detector baseline vs Naive Bayes
Building AI course project

## Summary
This project describes (and optionally prototypes) a simple email spam detector.
It compares a strong baseline (“always predict not spam”) against a basic ML pipeline
(bag-of-words or TF-IDF + Naive Bayes) and explains how to evaluate it correctly.

## Background
Email spam wastes time, spreads scams, and can be dangerous.
A common pitfall is celebrating “high accuracy” even when the dataset is imbalanced
(e.g., most messages are not spam), so a majority-class baseline can look great.

Key questions:
- What baseline should the model beat to be worthwhile?
- How do we represent text as numbers?
- How do we avoid overfitting by evaluating on unseen data?

## How is it used?
Context:
- A user (or organization) receives emails/messages continuously.
- The system predicts spam vs not spam (or spam probability).
- Emails predicted as spam can be moved to a spam folder or flagged for review.

Users and affected people:
- End users (missed important emails if false positives happen).
- Organizations (security and productivity).
- Potentially also senders (risk of legitimate emails being filtered).

## Data sources and AI methods
### Data
Planned options:
- A public spam/ham dataset (to be added), OR
- A small personal dataset exported from an email inbox (after removing private info).

### Methods
Text representation:
- Bag-of-words counts, and/or
- TF-IDF weighting to reduce the impact of very common words.

Models:
- Baseline: always predict the majority class (“not spam”).
- Naive Bayes classifier trained on the text vectors.

Evaluation:
- Train/test split (no overlap).
- Report accuracy, but also consider precision/recall (spam is usually the minority).

## Challenges
- Class imbalance: accuracy alone can be misleading.
- Privacy: real emails may contain sensitive information.
- Distribution shift: spam tactics change over time.
- False positives are costly (important emails could be lost).

## What next?
- Add a small working demo (training + prediction script).
- Compare Naive Bayes vs logistic regression.
- Add a confusion matrix and precision/recall metrics.
- Experiment with preprocessing (lowercasing, stop-words, lemmatization).

## Acknowledgments
- Inspired by the Elements of AI / Building AI course final project format.
- If datasets, libraries, or code are added later, they will be credited here.
