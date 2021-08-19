# Hackbio_Internship_Training
HackBio Internship Stage 2 Drug Discovery with Machine Learning and Data Analysis
# Step 1
In this step, our target protein, acetylcholinesterase is searched for on the ChEMBL database using the chembl websource client python library, in order to retrieve its bioactivity data, on which operations and processes will subsequently be performed. Once the data is retrieved, preprocessing is done, including dropping missing values, or duplicates, and segregating the data into categories according to their bioactivity threshold, from which the curated data is obtained.
# Step 2
The SMILES notations from the data retrieved is cleaned and Lipinski's descriptors are calculated. Further, Exploratory Data Analysis is performed.
# Step 3
Fingerprint descriptors using PADEL-descriptor are calculated and tabulated.
# Step 4
Involves output data visualisation using pandas,seaborn and Scikit-learn.

Feature extraction

Model used RandomForestRegressor imported from scikit-learn

Data split into Training and Validating using scikit-learn.

Scatterplot generated using matplotlib imported from seaborn.
