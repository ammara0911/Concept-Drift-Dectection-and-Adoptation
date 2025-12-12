# Concept-Drift-Dectection-and-Adoptation



\## Overview



This project addresses the problem of \*\*concept drift\*\* in long-running NLP systems, where the style or meaning of text changes over time and models trained earlier start making errors. Instead of waiting for labels—which often arrive slowly—the project monitors \*\*changes in model embeddings\*\* over time to detect drift.



The approach compares each new chunk of text with a stable reference set using \*\*five different distance measures\*\*. These signals are standardized and tracked using a \*\*CUSUM rule\*\*, so only sustained changes trigger a drift alert. Once drift is detected, the model is updated with a small \*\*LoRA module\*\* rather than retraining the entire model from scratch.



Tests on sequential slices of the \*\*Yelp dataset\*\* showed that drops in the classifier’s F1 score align well with the drift signals, and that the lightweight LoRA update usually restores performance efficiently.



---



\## Files



\- `embedding-based-drift.ipynb` : Jupyter notebook containing experiments, visualizations, and analysis  

\- `README.md` : Project description  



---



\## How to Run



1\. Clone the repository:


git clone https://github.com/ammara0911/Concept-Drift-Dectection-and-Adoptation.git



Author

Ammara Arshad

