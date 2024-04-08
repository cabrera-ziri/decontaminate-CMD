Here I keep different ways to decontaminate the CMD of a cluster, based only on the photometry of the field and cluster regions.

1. decontaminate_ngc419.ipynb: is the method presented in [Cabrera-Ziri et al. (2020)](https://ui.adsabs.harvard.edu/abs/2020MNRAS.495..375C/abstract) based on statistical decontamination of CMD.

2. first_pop_classifier.ipynb: Proof-of-concept random forest classifier based on perfect membership labels. This will be developed to be trained on mock data (i.e. real world labels).

3. pop_classifier.ipynb: Based on first_pop_classifier. But:
    - From a sample of (mostly) cluster stars and (mostly) field stars, defined from the centre and outskirts of the cluster.

    ![m4 starting samples](figures/starting_samples.png "m4 starting samples")

    - Then we model the cluster and field CMD using GMM.

    ![mock cluster CMD](figures/mock_cluster_CMD.png "mock cluster CMD")

    - Distribute field stars uniformly in space. For cluster stars follow the Plummer model of the cluster radius.
    - Train the classifier on this mock data and check performance. *It's very important that spatial footprint is similar to data!!!*.
    
This is an example of first_pop_classifier on M4 data set:

![m4 cleaned](figures/m4_cleaned.png "m4 cleaned")

This is the confusion matrix for this dataset:

![m4 confusion matrix](figures/m4_confusion_matrix.png "m4 confusion matrix")

## To do:

1. first_pop_classifier.ipynb
    - Try a simple decission tree
    