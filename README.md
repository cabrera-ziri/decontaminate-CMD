Here I keep different ways to decontaminate a cluster's CMD based only on the photometry of the field and cluster regions.

## To do:

1. first_pop_classifier.ipynb
    - Try a simple decission tree
2. emp_pop_classifier.ipynb
    - From a sample of (mostly) cluster stars and (mostly) field stars defined from the centre and outskirts
    of cluster, get a model of cluster and field CMD.
    - Distribute uniformly in space field stars. For cluster stars follow Plummer model of the cluster's radius
    - Train classifier using this mock data and check performance
    - Apply classifier on real data
    