# Capstone: Log Classification using Supvervised Machine Learning

Overall, the following depicts the training/testing results


|          Accuracy: 1.0 |           |        |          |         |
|-----------------------:|:---------:|:------:|:--------:|--------:|
| Classification Report: | precision | recall | f1-score | support |
|                      0 |   1.00    |  1.00  |   1.00   |    7216 |
|                      1 |   1.00    |  1.00  |   1.00   |    5160 |
|                        |           |        |          |         |
|               accuracy |           |        |   1.00   |   12372 |
|              macro avg |   1.00    |  1.00  |   1.00   |   12372 |
|           weighted avg |   1.00    |  1.00  |   1.00   |   12372 |


![Classifier Confusion Matrix](assets/confusion_matrix.png)

---
### Notebook
Open jupyter notebook in:
- [nbviewer.org](https://nbviewer.org/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)
- [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)

***
## Data Overview

The raw log data used for this project was sourced from [Dreamhosters Log Sharing](https://log-sharing.dreamhosters.com) (Bundle 1). Among the logs available, the Linux system messages log and Apache HTTP access log (`access_log`) were selected, as they represent two of the most commonly encountered log types.

While the original tarball, `hnet-hon-var-log-02282006.tgz`, exceeds 100MB and is not included in this repository, a subset of the logs has been extracted and packaged as `raw_logs.tgz`. The logs are preserved in their original format for use in this project. Additionally, a sample dataset (`dataset.csv`) generated during the data preparation phase is also provided.

## Artifacts

| Artifact                              | Description                                      |
|---------------------------------------|--------------------------------------------------|
| `raw_logs.tgz`                        | Selected system and web logs in original form    |
| `dataset.csv`                         | Sample dataset derived from logs                 |
| `sctp_caps_log_classifier.pptx`       | Capstone project presentation deck               |
| `sctp_ml_log_data_RandomForestClassifier.ipynb` | Jupyter notebook documenting the model development |

## Observations

1. **Data Imbalance**: The dataset contains messages and `access_log` logs in a 2:3 ratio.
2. **Log Length Variability**: On average, logs are approximately 180 words long, though some logs exceed 8,000 words.
3. **Nature of Log Data**: Logs are often cryptic and do not follow natural language patterns, making traditional NLP cleaning techniques unsuitable.
4. **Model Performance**: The RandomForestClassifier model demonstrated its capability to classify log types with impressive performance metrics:
   - Training & testing accuracy: 100%
   - F1-score: 1.0
   - On a small set of "unseen" logs, accuracy dropped to 76%, highlighting potential limitations with generalization (as detailed in the Jupyter notebook).

## Key Insights

- **Data Diversity**: Increasing the variety and volume of log data from different sources is critical for improving model performance.
- **Scalability Challenges**: Introducing new log types requires custom logic, which may limit the flexibility and scalability of the system over time.
- **Model Explainability**: The RandomForestClassifier offers a transparent, interpretable structure, making it easier to understand how the model arrives at decisions.
- **Iterative Process**: Machine learning is inherently iterative. The workflow evolved with each iteration, allowing for continuous improvement through troubleshooting.

## Lessons Learned

Looking back, there are several key takeaways:

1. **Workflow Improvement**: A more robust and flexible pipeline is needed to handle diverse data sources at scale.
2. **Domain Knowledge**: While understanding the characteristics of the dataset is essential, this project exposed the gaps in domain expertise that could have led to better outcomes.
3. **Learning Through Troubleshooting**: Challenges such as environment instability and researching documentation contributed to valuable learning experiences, albeit indirectly.

## Future Directions

To enhance the current approach, several steps are planned for future iterations:

- **Dimensionality Reduction**: Explore introducing PCA achieve an optimum TfidfVectorize size
- **Model Exploration**: Investigate XGBoost as a potential alternative to RandomForestClassifier for comparison.
- **Data Expansion**: Incorporate log data from a wider range of sources to exponentially increase the dataset's diversity.
- **Automation with Deep Learning**: Explore deep learning techniques to automate the adaptation of the model to new log types, thereby improving scalability and efficiency.


***
Connect with me [LinkedIn](https://www.linkedin.com/in/franklinchui/) 


