# SCTP Capstone Project

### Log Classifier with RandomForestClassifier

[SCTP Capstone Log Classifier (nbviewer.org)](https://nbviewer.org/github/fc510/sctp-caps-log-classifier/blob/405bd61e91733c6a9bb275d60044d1ecc9f1cf95/sctp_ml_log_data_RandomForestClassifier.ipynb)


Collect 2 types of logs from [data source](https://log-sharing.dreamhosters.com/), namely system `messages` and httpd (web) `access_log` logs. They are combined and labeled **system_messages** and **httpd_access_log** respectively.

General overview of tasks:
- clean (eg removing non-ascii characters)
- normalize date and time feature into it's components
- pre-process the log data (`content` column)
- vectorized
- divide dataset into train-test-split
- train model
- evaluate model performance
- deploy model for inference (gradio)

Other tasks:
- hyperparameter tuning of baseline model
- compare with another classifier (eg Support Vector Machine)
- adjust/mine dataset for more features

### Insights

### Lesson Learnt

### Potential Enhancements
