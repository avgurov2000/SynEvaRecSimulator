# SynEvaRecSimulator

<h1 align="center"> Performance Ranking of Recommender Systems on Simulated Data
<h3 align="center">This work is an addition to the paper "Performance Ranking of Recommender Systems on Simulated Data" by Stavinova et al.</h3>

## Abstract
Recent studies have shown that modelling and simulation of interactions between a recommender system (RS) and its users have a great potential for accelerating the research and industrial deployment of RSs. Frameworks providing such simulations are called simulators and are widely used for RSs of different types. 
  
Nevertheless, there exist the problem of simulation validation and of the inconsistency of RS performance ranking on real-world and the corresponding synthetic data. 
In this paper, using and extending the recently developed SynEvaRec simulator we propose a validation procedure for simulators of this type and study the consistency of RS performance ranking on response matrices of different sparsity. 
  
It is observed in our experiments that (i) the procedure is an effective tool to see what one may expect from the simulation on real-world data, (ii) the consistency  of RS performance ranking depend on the data considered and even the sample size used for RS training.

## Structure
The repository has the following folders:
  - data. Contains the real-world dataset. (see Data section)
  - data_generators. Contains synthetic data generators
  - modules. Contains sourse code of the models used duting experiments.
  - notebooks. Contains experiments (see Experiments section).
  - synthetic_data. Contains synthetic datasets.
  
 Besides this, there are two Jupyter notebooks with examples of the models used duting experiments (AutoRec.ipynb, CollobarativeModel.ipynb).

## Data
We use two types of datasets in the study:
 - Validation data. The Validation dataset contains 1,000 users and 100 items (both with attributes), and 100,000 user-item responses (i.e. the data is complete). 
   Each user and each item has three attributes, all of them are numeric.
 - The real-world data. The dataset is a small one containing data about Restaurants and Their Clients (available <a href='https://www.kaggle.com/uciml/restaurant-data-with-consumer-ratings'>here</a> ).

Validation data is generated during experimentation with default settings.

## Experiments

Experiments are a set of Jupyter notebooks.
All experiments are available in their respective folders:
  
For Validation dataset:
```
./notebooks/validation/ValidationPerformance.ipynb
./notebooks/validation/ValidationSurfaceDense.ipynb
./notebooks/validation/ValidationSurfaceSparce.ipynb
```
For Restaurants dataset:
```
./notebooks/rests/RestPerformance.ipynb
./notebooks/rests/RestSurfaceDense.ipynb
./notebooks/rests/RestSurfaceSparse.ipynb
```
  
Each of the notebooks (in order) contains an experiment with quality hierarchy, quality surfaces for dense data, quality surfaces for sparse data for the corresponding dataset.
