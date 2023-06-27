# Ensemble Region-Specific GMMs for Subduction Earthquakes

## Table of Contents

+ [Overview](#overview)
+ [Abstract](#abstract)
+ [Install the requirements](#install)
+ [Citation](#citation)


## Overview
This folder contains the saved trained ML models on the NGA-Sub dataset. The showcase code is provided to as a sample of how to load the saved model and to create the ensemble model. Also some examples are provided to show how to plot the distance scaling and response spectra.
Since a pipeline framework has been used in Python, there is no need to process/normalize the input data for prediction and the saved models using pipeline take care of this step. The example in the showcase code is self-explanatory.

## Abstract <a name = "abstract"></a>
This study attempts to develop data-driven global and region-specific ground motion models (GMMs) for subduction earthquakes by ensemble modeling four different nonparametric supervised machine learning algorithms including Artificial Neural Network, Kernel-Ridge Regressor, Random Forest Regressor, and Support Vector Regressor. To achieve this goal, we train the model by using a subset of the NGA-Sub dataset including 9124 recordings out of 150 interface and intraslab earthquakes recorded at 3134 different stations. A grid search is used to find the best hyperparameters for each model. The proposed model considers magnitude, rupture distance, VS30, and ZTOR as well as tectonic and region as input parameters, and predicts various median ground motion intensity measures such as peak ground displacement (PGD), peak ground velocity (PGV), peak ground acceleration (PGA), and 5%-damped pseudo-spectral acceleration (PSA) values at spectral periods of 0.01 to 10 sec in log scale. The response spectra as well as the distance and magnitude scaling trends are consistent and comparable with the global NGA-Sub GMMs with slightly lower standard deviations. A mixed effects regression analysis is used to partition the total aleatory variability into between-event, within-station, and event-site-corrected components. The derived GMMs are applicable for interface and intraslab earthquakes with moment magnitudes ranging from 4.58 to 9.12 and rupture distances up to 1000 km for sites having VS30 values between 95 and 2230 m/sec.

## Install the requirements <a name = "install"></a>
* Python 3.9 and higher is required
* Create a virtual environment: conda create -n <env_name> python=3.9
* Activate the virtual environment: conda activate <env_name>
* Intall all dependencies using pip, run the command: pip install -r requirements.txt
```ShellSession
$ conda deactivate
$ conda create -n GMM python=3.9.13 anaconda
$ conda activate GMM
```
Then, install the requirements:
```ShellSession
$ pip install -r requirements.txt
```

## Citation <a name = "citation"></a>
Sedaghati, F. and S. Pezeshk, (2023). Ensemble Region-Specific GMMs for Subduction Earthquakes, Seismological Research Letters
