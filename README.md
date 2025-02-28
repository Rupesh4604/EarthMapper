# EarthMapper #

Project repository for EarthMapper.  This is a toolbox for the semantic segmentation of non-RGB (i.e., multispectral/hyperspectral) imagery.  We will work on adding more examples and better documentation.

## Description ##

This is a classification pipeline from various projects that we have worked on over the past few years.  Currently available options include:

### Pre-Processing ###
* MinMaxScaler - Scale data (per-channel) between a given feature range (e.g., 0-1) 
* StandardScaler - Scale data (per-channel) to zero-mean/unit-variance
* PCA - Reduce dimensionality via principal component analysis
* Normalize - Scale data using the per-channel L2 norm

### Spatial-Spectral Feature Extraction ###
* Stacked Convolutional Autoencoder (SCAE)
* Stacked Multi-Loss Convolutional Autoencoder (SMCAE)

### Classifiers ###
* SVMWorkflow - Support vector machine with a given training/validation split
* SVMCVWorkflow - Support vector machine that uses n-fold cross-validation to find optimal hyperparameters
* RandomForestWorkflow - Random Forest classifier
* MLP - Multi-layer Perceptron Neural Network classifier
* SSMLP - Semi-supervised MLP Neural Network classifier

### Post-Processors ###
* Markov Random Field (MRF)
* Fully-Connected Conditional Random Field (CRF)

## Dependencies ##
* Python 3.5/3.7 (We recommend the [Anaconda Python Distribution](https://www.anaconda.com/download/))
* numpy, scipy, and matplotlib
* [scikit-learn](http://scikit-learn.org/stable/)
* [spectral python](http://www.spectralpython.net/) (spectral 0.23.1)
* [gdal](http://www.gdal.org/) - conda install conda-forge gdal==3.5.2
* [tensorflow](https://www.tensorflow.org/) (tensorflow 1.14) 
* [pydensecrf](https://github.com/lucasb-eyer/pydensecrf) (pydensecrf 1.0)
* [gco_python](https://github.com/amueller/gco_python)
  (pip instal pygco) (pygco 0.0.16)

## Instructions ##

### Installation ###
```console
$ python setup.py
```
### Run example ###
```console
$ python examples/example_pipeline.py
```
### Acknowledgment and Credit ###

We give full credit to the author of the repository, [Ronald kemker](https://github.com/rmkemker), for the code and implementation of the research paper: *Kemker, R., Gewali, U. B., Kanan, C. - "EarthMapper: A Toolbox for the Semantic Segmentation of Remote Sensing Imagery." 
