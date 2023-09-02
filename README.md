# MiXSleepNet

Code of the paper 'MixSleepNet: A Multi-Type Convolution Combined Sleep stage classification Model'.
## Dataset

The ISRUC dataset can be downloaded on the official website: https://sleeptight.isr.uc.pt/?page_id=76

## How to run
### 1. Modify configuration files

Modify configuration files especially paths in each config file.
    
    The `data` item in `original` of the `data_set.json` is the path of .mat files.
    The `label` item in `original` of the `data_set.json` is the path of .txt label files.
    The `data` item in `formatted` of the `data_set.json` is the path of .mat files (same value with the data item in the original one).
    The `label` item in `formatted` of the `data_set.json` is the path of .txt label files (same value with the label item in the original one).
    The `save_path` item in `preprocess.json` is the path to save preprocessed data.
    The `preprocessed_data_save_path` item in `feature_extraction.json` is the path to save preprocessed data.
    The `extracted_feature_save_path` item in `feature_extraction.json` is the path to save extracted features.
    The `save_path` item in `train.json` is the path to save the trained model files.

All paths above are folders.

### 2. Preprocess

Run `preprocess_isruc_s3.py` by `python preprocess_isruc_s3.py`

This program will preprocess and save preprocessed data to the folder 'preprocessed_data'.

### 3. Feature extraction

Run `feature.py` by `python feature.py`

This program will extract features and save them to folder 'extracted_features'.

### 4. Train

Run `train.py` by `python train.py`

This program will train models and save them to a new folder under 'result'.

### 4. Evaluate

Run the `evaluate.py` file located in the new created folder, which is under the 'result' folder.

This program will evaluate models.
