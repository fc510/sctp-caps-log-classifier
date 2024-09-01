# SCTP Capstone Project

### Log Classifier with RandomForestClassifier

[SCTP Capstone Log Classifier (nbviewer.org)](https://nbviewer.org/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)

Collect 2 types of logs from [data source](https://log-sharing.dreamhosters.com/), namely system `messages` and httpd (web) `access_log` logs. They are combined and labeled **system_messages** and **httpd_access_log** respectively.

The log data are:
- clean (eg removing non-ascii characters)
- normalize date and time feature into it's components
- pre-process the log data (`content` column)
- vectorized
- train-test-split

### Insights

### Lesson Learnt

### Potential Enhancements
