# Search for exoplanets

This is the main project directory.

## Examples

#### TensorBoard
Our model configuration is stored in astronet/astronet/exo_nn_model. To see our model performances while it was training, you can just
```
tensorboard --logdir path/to/exo_NN/astronet/astronet/exo_nn_model
```

### Whole process
(Documentations are as comments inside code)

#### Download Kepler data
To download Kepler data corresponding to the data/csv/dr24_tce.csv, you can run the following script
```
./data/generate_download_script.sh
```
which will prepare the get_kepler.sh script and download around 90GB of tdata from Kepler lightcurves.

#### Generate input records
To process lightcurves and generaate valid input records for CNN, you can use
```
./scripts/generate_inputs.sh
```
See its documentation for the inputs it must take.

#### Train model
To train our model, use
```
./scripts/train.sh [...]
```
See its documentation for the inputs it must take.

#### Test model
To test the model, use 
```
./scripts/test.sh [...]
```
See its documentation for the inputs it must take

### Predict
To make a prediction for your candidate, use
```
./scripts/predict.sh [...]
```
See its documentation for the inputs it must take.

