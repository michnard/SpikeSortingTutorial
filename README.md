# SpikeSortingTutorial
Short tutorial on how to sort spikes from LFP data.

The main procedure can be found in the notebook "Spike Sorting.ipynb".

The procedure is standard (https://doi.org/10.1016/j.brainresbull.2015.04.007):
1) band pass filtering (300~3000 Hz) using a 2nd order Butterworth filter
2) robust median absolute deviation to detect spikes
3) feature extraction using PCA (3features per channel)
4) spike sorting using mixture of gaussians


The data used in the notebook can be downloaded here: https://drive.google.com/file/d/1jnKv4zf-8l5ubCmXZDk6HzuwNF7aCK9S/view?usp=sharing
Alternatively, the same data can be generated using the notebook "Generate_Data.ipynb".
This will create a binary file with 4 digitalized LFP channels, which consist of spikes, oscillations and noise.

Requirements:
Python 3.7, notebooks to be opened in jupyter notebook (follow instructions here to install: https://docs.anaconda.com/anaconda/install/).
Packages required: numpy, scipy, matplotlib, scikit-learn (0.24.2)
optional: MulticoreTSNE

Note: to install MulticoreTSNE use, from terminal, the command "pip install cmake MulticoreTSNE".
