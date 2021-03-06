# HackBio Internship Training
HackBio Internship Stage 2 Drug Discovery with Machine Learning and Data Analysis
# Step 1
The CDD_ML_Part_1_Acetylcholinesterase_Bioactivity_Data_Concised.ipynb file must be run cell by cell.

In this step, our target protein, acetylcholinesterase is searched for on the ChEMBL database using the chembl websource client python library, in order to retrieve its bioactivity data, on which operations and processes will subsequently be performed. Once the data is retrieved, preprocessing is done, including dropping missing values, or duplicates, and segregating the data into categories according to their bioactivity threshold, from which the curated data is obtained.
# Step 2
The CDD_ML_Part_2_Acetylcholinesterase_Exploratory_Data_Analysis.ipynb file must be run cell by cell.

The SMILES notations from the data retrieved are cleaned. Lipinski's descriptors are calculated with the help of defining a custom function, resulting which the outputs of molecular weights, log P (octanol-water partition coefficient), number of H-donors and the number of H-acceptors. The values of IC50 are converted into pIC50 so as to get a better distribution in the plot. Further, Exploratory Data Analysis is performed after removal of the intermediate bioactivity class defined in Step 1, and frequency, scatter and box plots are created. Statistical analysis is performed. 
# Step 3
The CDD_ML_Part_3_Acetylcholinesterase_Descriptor_Dataset_Preparation.ipynb file must be run cell by cell.

The loaded csv file is further filtered and the chemical structures are cleaned by removing salts and small organic acids in order to remove ay impurities. The output consists of PubChem fingerprints using PADEL-descriptor, which are calculated and tabulated. The data is shifted and rearranged, so as to serve as a more convenient input for Step4.
# Step 4
The CDD_ML_Part_4_Acetylcholinesterase_Regression_Random_Forest.ipynb file must be run cell by cell.

The input file consists of the PubChem fingerprints retrieved in Step 3. Now, PubChem fingerprints are being used, as Lipinski's descriptors have a global approach to deducing the molecule's properties, whereas the PubChem fingerprints give us more of a localized approach. The data is separated into input X and Y dataframes. The data is cleaned up further by removing low variance features, and is split in the 80-20 ratio as train and test sets respectively. A regression model is generated using RandomForestRegressor, imported from the scikit-learn package, after which a scatter plot of experimental vs. predicted outputs is displayed with the use of matplotlib package.. It requires data visualization using the pandas, seaborn and sckit-learn packages.
# Step 5
The CDD_ML_Part_5_Acetylcholinesterase_Compare_Regressors.ipynb file must be run cell by cell.

In this step, LazyPredict library is used to compare several machine learning algorithms to build regression models of the acetylcholine inhibitors. LazyPredict library gives a quick and rapid model building of classification and regression models in only a few lines of code. The dataset is split into X and Y variables, preprocessed by removing low variance features and splitting into Train and Test data sets with an 80:20 ratio respectively. 
To build the model, the machine learning algorithm is assigned into a classifier variable, then assigning the results from the prediction after the model has been built to the Train and Test variables.
Model building uses default parameters for all algorithms used; in our case, 42 algorithms. After the models have been built, comparison of the Train and Test sets from prior model libraries used begins. Data visualization of the performance gives a bar-plot of R-squared values and therefore, we compare RMSE values and calculation time. The longer the bars, the longer the time it takes to build the model. 
# Step 6
Running the application requires running the bioactivity_prediction_app file to be run on a Google Colab file and Jupyter to generate the descriptors_list, as well as running the python script of app.py on the anaconda prompt termminal, in order to host the streamlit app in a web browser. The python script uses the PADEL-descriptor function to calculate the pIC50 of the test dataset in .txt format, the output of which is generated as a prediction.csv file, containing the prediction results. The image logo function is used as an outlook of the web app.
To replicate such, run the prediction notebook to generate the pickle file and run the python script using #streamlit run app.py on the terminal to host the web application on the browser and try predictions. We then were able to download the prediction file using the Web app, and uploaded screenshots of it running. A screenshot of the anaconda terminal running script has been uploaded for assistance.

This step entails deploying our model built in Step 4 into a web application. There are several ways to deploy a model, but the tutorial adopted a method of deploying such that, to make a prediction, we input our text file which is the SMILES annotation and the ChemBL ID and predict the pIC50 of the compound to check whether it is within the range of approved pIC50 of compounds that inhibits our target receptor Acetycolinesterase in Alzheimer'S.
The model used to make prediction is generated as a pickle file but too large to be uploaded, the model is represented as a random forest model zipped file and uploaded.


The source of the tutorial is https://www.youtube.com/watch?v=jBlTQjcKuaY titled Python for Bioinformatics - Drug Discovery Using Machine Learning and Data Analysis

The codes and output and input csv files are included and retrieved, and all the cells must be run. The outputs are shown. The instructions to run the web application are given above.

Please find the contributors list below.

Max (@Max)- Part 1 Data Curation, Preprocessing, Retrieval  Coding, final edits to readme file

Priyanka (@PriyankaPandit) - Part 1 Data Curation, Preprocessing, Retrieval  Coding

Vishnupriya (@Vishnupriya)- Part 1 Data Curation, Preprocessing, Retrieval Coding


Ojei (@Ojei)- Part 2 Exploratory Data Analysis Coding

Prashik (@prashikkk)- Part 2 Exploratory Data Analysis Coding

Sochi (@Sochi)- Part 2 Exploratory Data Analysis Coding

Ugochi (@Ugochi)- Part 3 Descriptors Calculation Coding

Maargavi (@Maargavi)- Part 3 Descriptors Calculation Coding

Shangari (@Shangari17)- Part 3 Descriptors Calculation Coding

Josiah (@Josiah)- Part 4 Model Building

Hesborn (@Hesborn)- Part 4 Model Building, Part 1 to 6 error assistance and resolving

Chwayita(@ChwayitaM) - Part 5 Model Comparison coding

Diya (@DiyaArul)- Part 5 Model Comparison Coding, comments and instructions addition, final edits

Xavier (@Xaviwho)- Part 5 Model Comparison Coding

Samar (@Samar)- Part 6 Model Deployment Coding

Zainab (@Zainab)- Part 6 Model Deployment Coding

Final edits consisted of having to reupload program files after making appropriate edits.
