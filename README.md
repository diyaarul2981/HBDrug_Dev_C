# HackBio Internship Training
HackBio Internship Stage 2 Drug Discovery with Machine Learning and Data Analysis
# Step 1
In this step, our target protein, acetylcholinesterase is searched for on the ChEMBL database using the chembl websource client python library, in order to retrieve its bioactivity data, on which operations and processes will subsequently be performed. Once the data is retrieved, preprocessing is done, including dropping missing values, or duplicates, and segregating the data into categories according to their bioactivity threshold, from which the curated data is obtained.
# Step 2
The SMILES notations from the data retrieved are cleaned. Lipinski's descriptors are calculated with the help of defining a custom function, resulting which the outputs of molecular weights, log P (octanol-water partition coefficient), number of H-donors and the number of H-acceptors. The values of ic50 are converted into pic50 so as to get a better distribution in the plot. Further, Exploratory Data Analysis is performed after removal of the intermediate bioactivity class defined in Step 1, and frequency, scatter and box plots are created. Statistical analysis is performed. 
# Step 3
The loaded csv file is further filtered and the chemical structures are cleaned by removing salts and small organic acids in order to remove ay impurities. The output consists of PubChem fingerprints using PADEL-descriptor, which are calculated and tabulated. The data is shifted and rearranged, so as to serve as a more convenient input for Step4.
# Step 4
The input file consists of the PubChem fingerprints retrieved in Step 3. Now, PubChem fingerprints are being used, as Lipinski's descriptors have a global approach to deducing the molecule's properties, whereas the PubChem fingerprints give us more of a localized approach. The data is separated into input X and Y dataframes. The data is cleaned up further by removing low variance features, and is split in the 80-20 ratio as train and test sets respectively. A regression model is generated using RandomForest, after which the a scatter plot of experimental vs. predicted outputs is 
Involves output data visualisation using pandas,seaborn and Scikit-learn.

Feature extraction

Model used RandomForestRegressor imported from scikit-learn

Data split into Training and Validating using scikit-learn.

Scatterplot generated using matplotlib imported from seaborn.
# Step 5
In this step, Lazypredict library is used to compare several machine learning algorithms for building regression models of our acetylcholine inhibitors. Lazypredict library gives a quick and rapid model building of classification and regression models in few lines of code. The data set is split into X and Y variables, cleaned up by removing low variance features and split into Train and Test data sets with an 80:20 ratio respectively. 
To build the model, the machine learning algorithm is assigned into a classifier variable, then assigning the results from the prediction after the model has been built and assigning it to the Train and Test variables.
Model building uses default parameters for all algorithms used; in our case, 39 algorithms. After the models have been built, comparison of the Train and Test sets from prior model libraries used begins. Data visualization of the performance gives a bar-plot of 'R-suared' values and thus we compare RMSE values and Time taken/Calculation time. The longer the bars, the longer the time it takes to build the model. 
# Step 6
This is basically deploying our model built in step 4 into a web application. There are several ways to deploy a model but the tutorial adopted a method of deploying the model to a web application to make a prediction whereby we input our text file which is the smiles annotation and the ChemBL ID and predict the pIC50 of the compound to check whether it is within the range of approved pIC50 of compounds to binds to the target receptor Acetycolinesterase.
The model used to make prediction is generated as a pickle file but too large to be uploaded, the model is represented as a random forest model zipped file and uploaded.
The bioactivity_prediction_app notebook was run on google colab and jupyter to generate the descriptors_list. 
The logo to be used on the web app is as designed in the sample tutorial and uploaded as logo_png.
