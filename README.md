# DeepAR Evaluation

This repository contains code to evaluate DeepAR model on M3, M4, Tourism, Electrcity and Traffic datasets.

## How to run

For non-GPU environment change mxnet version in `requirements.txt` by replacing `mxnet-cu102==1.6` 
with `mxnet==1.6`.

The `Makefile` is built to run experiments locally, what may take a lot of time; for cloud/cluster 
infrastructures change the `Makefile` to deploy and run according to your environment. 

### Build and test

```shell script
make build
make test
```

### Run experiments

Run all experiments

```shell script
./run_all.sh <ensemble-size> deepar Makefile
```

To run one experiment look at commands in `run_all.sh`

### Get statistics

See notebooks in `notebooks` directory for ensembles.

For individual experiments load forecasts from `storage/deepar/<experiment>/forecasts/*.npy` and pass them
to the `evaluate` method of the corresponding dataset instance, see examples in `test/datasets/*.py`


