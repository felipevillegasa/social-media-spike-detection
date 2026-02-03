# Real-Time Social Media Spike Detection & Topic Spike Analyzer

This project presents a real-time system for detecting and explaining unexpected spikes in social media activity.
It combines time-series anomaly detection with topic modeling to identify *when* abnormal behavior occurs and *why* it happens.

---

## Project Context
This project was developed as part of a graduate practicum in collaboration with a social media management platform.
The public version shared in this repository was approved for academic submission and does not include proprietary data,
internal systems, or confidential information.

---

## System Overview
The system is composed of three main components:

- **Volume Spike Detector**  
  Detects abnormal increases in interaction volume using Prophet-based time-series baselines with rolling training windows.

- **Negative Sentiment Spike Detector**  
  Identifies sudden shifts in negative sentiment even when total interaction volume remains stable.

- **Topic Spike Analyzer**  
  Explains detected spikes by surfacing the themes driving the anomaly using a historically trained BERTopic model.

Together, these components enable early crisis detection and interpretable explanations aligned with real-world events.

---

## Topic Spike Analyzer (My Contribution)
My primary contribution focused on the design and implementation of the **Topic Spike Analyzer**, including:

- Training a fixed BERTopic model on historical data to ensure topic stability across time.
- Implementing a delta-weighted topic comparison to highlight meaningful thematic deviations during spike windows.
- Developing an outlier clustering pass to surface emerging themes not present in the historical topic vocabulary.
- Evaluating robustness using a holdout-month strategy aligned with real-world events.

---

## Evaluation Strategy
Due to the absence of ground-truth labels, the system was evaluated using proxy-labeling strategies and qualitative validation:

- Percentile-based proxy labels for volume spikes.
- Recall and precision analysis for alert quality.
- Holdout-month evaluation to validate topic explanations against known external events.

---

## Full Technical Report
The complete technical report, including methodology, evaluation, and results, is available in this repo

---

## Tools & Technologies
- Python
- Prophet (time-series forecasting)
- BERTopic (topic modeling)
- NLP preprocessing pipelines
- Plotly (visualization)

---

## Notes
This repository focuses on system design and modeling logic.
Code and implementation details can be shared or extended.
