# SpikeSortingTutorial
Short and easy tutorial on how to sort spikes from LFP data

Python 3.7, notebooks to be opened in jupyter notebook.
Packages required: numpy, scipy, matplotlib, scikit-learn (0.24.2)
optional: MulticoreTSNE

Data is generated using the notebook "Generate_Data.ipynb". 
This will create a binary file containing 4 channels which contain spikes, oscillations and noise.

Afterwards, one can try and recover the spikes, sort them and compare with ground truth.
This is all done in the notebook "Spike Sorting.ipynb".

The procedure is standard:
1) band pass filtering (300~3000 Hz) using a 2nd order Butterworth filter
2) robust median absolute deviation to detect spikes
3) feature extraction using PCA (3features per channel)
4) spike sorting using mixture of gaussians
