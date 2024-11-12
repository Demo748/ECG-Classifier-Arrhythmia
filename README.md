# ECG-Classifier-Arrhythmia

Adapts [koen-aerts/ECG_ML](https://github.com/koen-aerts/ECG_ML) for importing the MIT-BIH dataset

### Data loading
Run download.py in ECG_ML/utils, populates ECG_ML/data/mitdb with raw files<br><br>


Run 02_import_mitdb_data.ipynb, processes and formats the raw files into csvs in data_ecg/mitdb

Run 04_prep_imported_data.ipynb, gathers all the data and splits into an 80:20 training:testing ratio<br><br>


Place canine data in SASH directory, including custom, data, labels folders provided in the SASH dataset

Run data_generator.ipynb in SASH/code to preprocess, format and output the canine data for training/testing<br><br>


test_canine_shuffled.csv, train_canine_shuffled.csv, test_human.csv and train_human.csv should now be created at the root directory

They can be downloaded from [my drive](https://drive.google.com/file/d/19oONq3yuIY12F9OO8xCAHK0xpFkFtgDV/view?usp=sharing) to save time<br><br>

### Training/Evaluation
Run cells in CNN_classifier.ipynb to load the desired preprocessed data, create the CNN, and either train or resume training an existing model, or just load a selected model for evaluation
