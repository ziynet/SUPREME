# SUPREME
SUPREME: A cancer subtype prediction methodology using Graph Convolutional Neural Networks

### How to run SUPREME?

You can use `SUPREME.py` or `SUPREME.ipynb` (for jupyter notebook users).

#### User Options

- Adjust the following variables:
  - `base_path`: the path to SUPREME github folder
  - `dataset_name`: the data folder name in `base_path` including required input data for SUPREME run
  - `node_networks`: list of the datatypes to use (should have at least 1 datatype)
  - `features_to_integrate`:  list of the datatypes to integrate as raw feature
  - `addRawFeat`: *True* or *False*: If *True*, raw features from listed datatypes in `features_to_integrate` will be integrated; if *False*, no raw features will be integrated.
- Adjust the following hyperparameters:
  Those hyperparameters are designed only for quick check. While running SUPREME for the real data, use the default values, or manually adjust them.
  - `max_epochs`: maximum number of epoch (default is 500.)
  - `min_epochs`: minimum number of epoch (default is 200.)
  - `patience`: patience for early stopping (default is 30.)
  - `learning_rates`: list of values to try as learning rate (default is [0.001, 0.01, 0.1].)
  - `hid_sizes`: list of values to try as hidden layer size (default is [16, 32, 64, 128, 256, 512].)
  - `xtimes`: the number of SUPREME runs for each hyperparameter combination (default: 10, should be more than 1.) 
