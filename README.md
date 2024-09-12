# Capstone: Log Classification using Supvervised Machine Learning

|          Accuracy: 1.0 |           |        |          |         |
| ---------------------: | :-------: | :----: | :------: | ------: |
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
The jupyter notebook [Capstone on Log Classification (nbviewer.org)](https://nbviewer.org/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)

***
### Dataset
Raw logs are obtained from `https://log-sharing.dreamhosters.com`, where linux system `messages` log and apache httpd web `access_log` logs were selected for this project. They are selected due to their distinction in their content purpose and by far some of most common log data available.

The raw logs exists in multiple copies (due to log rotation), they are first consolidated respectively, cleaned, pre-processed and thereafter labeled and combined into a single dataset (csv). This resulted in a dataset of over 60k log entries available.

***
### Observations

- The dataset is imbalanced between the `messages` and `access_log` logs in a 2:3 proportion
- In general log length average about 200 words, but there instances where log can be as long as over 8000 words
- Due to the nature of log data, it isn't exactly a natural language and using NLP cleaning technique may not be ideal since some info within log data are inherent cryptic
- Nonetheless, the RandomForestClassifier proves sufficiently capable to identify the log type
- The model perform well during training & testing achieving 100% accuracy, whereas during sampled inference test accuracy only managed over 70%

### Insights

- For each log type, having more labeled data containing more variety in log structure would certainly improve the model's performance
- However, the above is only achievable with well prepared log data for training, which is a huge endeavour in itself
- RandomForestClassifier (aka decision tree model) is intrinsic interpretable, and hence the explainability thru visualization is straightforward

### Lesson Learnt

- understanding the dataset's characteristics, helps to formulate a initial set of hyperparameters for model training and to avoid issues like environment crashing

### Going forward...

- try XGBoost for comparison of performance
- improve the dataset's representation of the different log type
- design a deep learning solution to automatically classify different log types at scale
- perhaps create a new feature to rate the "severity" of the log


***
Connect with me [LinkedIn](https://www.linkedin.com/in/franklinchui/) 


