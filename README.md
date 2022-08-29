# Smart-Meter-Anomaly-Detection
---Data Source--------------------------
The past outage history data was downloaded from Ausgrid

https://www.ausgrid.com.au/Industry/Our-Research/Data-to-share/Past-outage-data
The original outage data contain three months outage history records and provided as XLSX file format

---Experiment Environment---------------
Python           : 3.5.2
Keras            : 2.1.6
Tensorflow       : 1.13.1
Pandas           : 0.24.2
Scikit-learn     : 0.21.3
Imbalanced-learn : 0.5.0

---Experiment Step----------------------
1. Run xlsx_to_csv.ipynb for transfer the outage history XLSX file to a CSV file.

2. Run data_preprocess.ipynb for preprocessing the past outage data to a continuous hourly data contains non-outage and outage rows.

3. Run ADASYN_data_augmentation.ipynb for outage data augmentation(increase more outage data to balance the dataset).

4. Run LSTM_outage_predict_final.ipynb for training the LSTM model with the augmented dataset and test with the original dataset.

5. LSTM_outage_predict_single_layer.ipynb is used to train a single LSTM layer model for comparing the experimental result to the final LSTM model.
