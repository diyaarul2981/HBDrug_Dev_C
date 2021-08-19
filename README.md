# HackBio Internship Training
HackBio Internship Stage 2 Drug Discovery with Machine Learning and Data Analysis
# Step 1
In this step, our target protein, acetylcholinesterase is searched for on the ChEMBL database using the chembl websource client python library, in order to retrieve its bioactivity data, on which operations and processes will subsequently be performed. Once the data is retrieved, preprocessing is done, including dropping missing values, or duplicates, and segregating the data into categories according to their bioactivity threshold, from which the curated data is obtained.
# Step 2
The SMILES notations from the data retrieved are cleaned. Lipinski's descriptors are calculated with the help of defining a custom function, resulting which the outputs of molecular weights, log P (octanol-water partition coefficient), number of H-donors and the number of H-acceptors. The values of ic50 are converted into pic50 so as to get a better distribution in the plot. Further, Exploratory Data Analysis is performed after removal of the intermediate bioactivity class defined in Step 1, and frequency, scatter and box plots are created. Statistical analysis is performed. 
# Step 3
The loaded csv file is further filtered and the chemical structures are cleaned by removing salts and small organic acids in order to remove ay impurities. The output consists of PubChem fingerprints using PADEL-descriptor, which are calculated and tabulated. The data is shifted and rearranged, so as to serve as a more convenient input for Step 4.
# Step 4
The input file consists of the PubChem fingerprints retrieved in Step 3. Now, PubChem fingerprints are being used, as Lipinski's descriptors have a global approach to deducing the molecule's properties, whereas the PubChem fingerprints give us more of a localized approach. The data is separated into input X and Y dataframes. The data is cleaned up further by removing low variance features, and is split in the 80-20 ratio as train and test sets respectively. A regression model is generated using RandomForest, after which the a scatter plot of experimental vs. predicted outputs is 
Involves output data visualisation using pandas,seaborn and Scikit-learn.

Feature extraction

Model used RandomForestRegressor imported from scikit-learn

Data split into Training and Validating using scikit-learn.

Scatterplot generated using matplotlib imported from seaborn.
