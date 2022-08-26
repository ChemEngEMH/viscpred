# viscpred
ANN model for viscosity prediction
This ANN model predicts log10(viscosity in mPa s) at different temperatures based on the SMILES notation of molecules. 

USAGE:
The model requires atom module identification and counting as well as modularity of molecular graphs. Thus the steps to use it are:
1. Create a .csv file with a column with all SMILES of the molecules you want the prediction for, use no headers
2. Use the name of the file to run de script "getmodinputs.py" using the function 'modules_batch(smifile)', where smifile is your file title with .csv extension.
This will create a file named "ANNinputinputfile.csv" with all model modules count and modularity vlaues.
3. Create a .csv file with a list of temperature values, use no headers.
4. Use the "ANNinputinputfile.csv" and your temperatures file to run the script "viscosity_prediction.py" using the function 'predict(modfile, tempfile)', where modfile is the output from step 2, and tempfile is your temperatures file title with .csv extension. This will create a "resultsfile.csv" with the SMILES and predicted values at the different temperatures.
Alternatively, you can edit the 'ANNinputfile.csv' and insert a 'Temperature' column with temperature values for each molecule before the Modularity column (i.e. Modularity should be the last column). The use the function 'viscosity_prediction(modelinputs)', where modelinputs is the edited 'ANNinputfile.csv' file. This will create a "RESULTS.csv" file with the predicted values.
5. Enjoy and provide any feedback.

Please if you use this code cite as this:
Martinez-Hernandez, E., Zenteno, C., Valencia, D., Aburto, A. Prediction of viscosity of biomass-based molecules using atom modules and modularity as descriptors in neural network models. Submitted Ago 2022.


