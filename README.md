# SCTP Assoc AI/ML Developer Capstone Project

![Classifier Confusion Matrix](assets/confusion_matrix.png)

---
### Log Classifier with RandomForestClassifier
The jupyter notebook [SCTP Capstone Log Classifier (nbviewer.org)](https://nbviewer.org/github/fc510/sctp-caps-log-classifier/blob/main/sctp_ml_log_data_RandomForestClassifier.ipynb)

***
### Dataset
Various log data types are available at `https://log-sharing.dreamhosters.com`.

For the purpose of this project, 2 log types are selected; they are linux system `messages` and apache httpd `access_log` logs. They are selected due to their distinct different nature and purpose. 

They are combined and labeled **system_messages** and **httpd_access_log** respectively. The combined dataset has over 60,000 log entries.

Steps:
1. Get Data
2. clean Data
3. Pre-Process Data
4. Feature Extraction
5. Exploratory Data Analysis & Feature Extraction
6. Model Training/Testing & Evaluation
7. Model Deployment

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
### Observations & Lesson Learnt
- Though log data is predominantly textual, unexpected non-ascii characters is only discovered when the full log file is loaed
- 

### What I have learned

### What could have done better
Given the opportunities, I would certainly attempt to
- increase the dataset size
- shuffle the dataset before using it to train the model
- 


***
Connect with Me at [Linkedin](https://sg.linkedin.com) 

