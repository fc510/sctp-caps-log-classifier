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
- [Colab](https://colab.research.google.com/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)

***
### Data
Raw logs are obtained from `https://log-sharing.dreamhosters.com` (Bundle 1) as a tarball. Within which, the linux system `messages` log and apache httpd web `access_log` logs were selected for this project as they some of the most common logs available. 

The original tarball `hnet-hon-var-log-02282006.tgz` is is over 100MB and is not provided in this repository. Only the selected log types are retained and packaged as-is here as `raw_logs.tgz` in their original form.

As a sample, the `dataset.csv` generated during `Prepare Data` phase is provided.

#### Artifacts

| Artifacts                                     | Description                        |
|:----------------------------------------------|:-----------------------------------|
| raw_logs.tgz                                  | Selected system and web logs       |
| dataset.csv                                   | Sample dataset                     |
| sctp_caps_log_classifier.pptx                 | Capstone Project Presentation deck |
| sctp_ml_log_data_RandomForestClassifier.ipynb | Jupyter notebook                   |


***
### Observations

- The dataset is imbalanced; the `messages` and `access_log` logs in a 2:3 proportion
- In general log length average about 150 words, as compared to some extreme of over 8000 words
- Due to the nature of log data, it isn't exactly a natural language and using NLP cleaning technique may not be ideal since some info within log data are inherently cryptic or "unnatural"
- Nonetheless, the RandomForestClassifier proves sufficiently capable to identify the log type
- Overall, the model perform well during training & testing, achieving 100% accuracy and a F1-score of 1.0
- At the end of the project, a **small** sample of "unseen" logs were used to test the model, the accuracy however drops to 76% (as shown in the notebook)

### Insights

- For each log type, having more log data and from more diverse sources certainly improve the model's performance
- However, there is a need to create custom logic whenever a new log type is introduced, making the system design inflexible and probably unsustainable
- RandomForestClassifier (aka decision tree model) is intrinsically interpretable, making explainability much apparent
- the machine learning model training is an iterative process, the workflow evolves with each repitition and improvement made while troubleshooting issues 

### Lesson Learnt

On the hindsight, I think
- A more robust strategy is needed to create a better workflow/pipeline to easily adapt to different data source at scale
- Though understanding the dataset's characteristics is crucial, but given this is the first individual exercise, I lack the domain experience and knowledge to do better
- However, time spent in troubleshooting issues like the "environment keep crashing", and sifting through more documentations, indirectly leads to some fruitful learning 

### Going forward...

- For comparison, XGBoost is a good candidate to try out
- Have more diverse sources of log data and expoentially increase the quantity
- Explore deep learning techniques to automate adapting new log type more efficiently


***
Connect with me [LinkedIn](https://www.linkedin.com/in/franklinchui/) 


