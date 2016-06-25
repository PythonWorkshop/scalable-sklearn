# Exploring scikit-learn with dask for scaling out computation on large data

## tl;dr

Here, you'll find demonstrations of scalable sklearn with [dask](http://dask.pydata.org/en/latest/) for out-of-core computation on large and complex datasets.  Dask uses task graphs (which are even modifiable) to scale out computation onto disk (out-of-core).  In this way both the computation and amount of data can be scaled in a big way which is really nice for ML.


## Blurb

It’s becoming increasingly important to scale up machine learning and deep learning computation either using a common solution in a cluster of GPUs or out-of-core computation on a single machine with enough local disk storage, which is rarely a problem these days.  Dask is a new library built on python that through out-of-core processes in task graphs can handle large datasets (gbs - tbs) for resource hungry computation.  It can do all this on a single PC/laptop given enough disk.

## Outline

1. Skimage to convert to numeric
* Standard scaling of data
* (Optional) clean up noise
* Image classification with 
  * MLP setup (using sklearn 0.18.dev0)
  * use dask and the partial_fit for MLP
* Visualize task graph
* Try it with gridsearchcv for hyperparameter tuning


