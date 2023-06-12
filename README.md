# CDH1-Cancer-Dis
ADD LINK TO PAPER.

## Reproducing Inference

### Requirements
- Python 3.8 or later
- CPU

### Setup
After cloning the repository to your local machine, install the code in editable mode from the repositories root directory `cdh1-cancer-dis/` by executing `pip install -e .`

### Test the setup
To test that the installation works, script a single aggregator model. A successful test should return `Created torchscripted checkpoint at <PATH>`. To run the setup test, execute the following command: 
```python -m cdh1_cancer_dis.model```


### Run the demo prediction
- 1. Script the ensemble model: 
  - `python -m cdh1_cancer_dis.script_ensemble`
  - This will create the torchscripted ensemble model we will require to run our demo predictions.
- 2. Predict the CDH1 on the provided demo embeddings using the torchscripted ensemble model:
  - `python -m cdh1_cancer_dis.predict`
  - The prediction step should print our the ground truth values, the model's continuous and binarized prediction. 
