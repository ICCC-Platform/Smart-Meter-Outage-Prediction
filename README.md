[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7134896.svg)](https://doi.org/10.5281/zenodo.7134896)
# Smart-Meter-Outage-Prediction
---Data Source-------------------------- <br />
The past outage history data was downloaded from Ausgrid <br />

https://www.ausgrid.com.au/Industry/Our-Research/Data-to-share/Past-outage-data <br />
The original outage data contain three months outage history records and provided as XLSX file format <br />

---Experiment Environment--------------- <br />
Python           : 3.5.2 <br />
Keras            : 2.1.6 <br />
Tensorflow       : 1.13.1 <br />
Pandas           : 0.24.2 <br />
Scikit-learn     : 0.21.3 <br />
Imbalanced-learn : 0.5.0 <br />

---Experiment Step---------------------- <br />
1. Run xlsx_to_csv.ipynb for transfer the outage history XLSX file to a CSV file.

2. Run data_preprocess.ipynb for preprocessing the past outage data to a continuous hourly data contains non-outage and outage rows.

3. Run ADASYN_data_augmentation.ipynb for outage data augmentation(increase more outage data to balance the dataset).

4. Run LSTM_outage_predict_final.ipynb for training the LSTM model with the augmented dataset and test with the original dataset.

5. LSTM_outage_predict_single_layer.ipynb is used to train a single LSTM layer model for comparing the experimental result to the final LSTM model.
