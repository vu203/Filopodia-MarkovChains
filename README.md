# Filopodia-MarkovChains

This analysis is part of a larger project on quantifying the dynamic behaviour of cellular protrusions called filopodia in microscopy data from cultured neurons.

We tracked the amount of accumulation (fluorescence) of a protein of interest in filopodial tips, and the movement of the tip. The question is whether the two time series describing fluorescence and movement are completely independent of each other, or whether there is evidence in the data supporting the notion that the two quantitites influence one another. 

The dataset we used contains time series data for 21 structures (filopodia), describing fluorescence and movement of each structure over up to 121 timepoins.

For each structure, we calculated the correlation over time between fluorescence and movement, and asked what is the likelihood of such correlation having been observed by chance. 

Fluorescence and movement in our time series display some extent of autocorrelation, which can be problematic for certain types of quantitative analysis. We used Markov chains to create models that plausibly recapitulate the fluorescence and movement behaviour over time (doing so separately for each of the 21 structures in the dataset), modelling fluorescence and movement independently of each other. This allowed us to run a large number of simulations (Markov chain realisations, all based on transition probabilities from real data for each filopodium); comparing the correlation between fluorescence and movement in these simulations with the correlation in the real-world data, we could assess the likelihood of observed correlations in real data having occured by chance.
