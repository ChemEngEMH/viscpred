# viscpred
ANN model for viscosity prediction.
This ANN model predicts log10(viscosity in mPa s) at different temperatures. 

USAGE:
1. Use the file named "ANNinputinputfile.csv" with all model modules count and modularity values.
2. Create a .csv file with a list of temperature values, use no headers. Or use the 'temperatures.csv' file provided as an example.
3. Use the "ANNinputinputfile.csv" and your temperatures file to run the script "viscosity_prediction.py" using the function 'predict(modfile, tempfile)', where modfile is the output from step 2, and tempfile is your temperatures file title with .csv extension. This will create a "resultsfile.csv" with the SMILES and predicted values at the different temperatures.
Alternatively, you can edit the 'ANNinputfile.csv' and insert a 'Temperature' column with temperature values for each molecule before the Modularity column (i.e. Modularity should be the last column). Then, use the function 'viscosity_prediction(modelinputs)', where modelinputs is the edited 'ANNinputfile.csv' file. This will create a "RESULTS.csv" file with the predicted values.
4. Enjoy and provide any feedback.

Please if you use this code cite as:
Martinez-Hernandez, E., Zenteno, C., Valencia, D., Aburto, A. Prediction of viscosity of biomass-based molecules using atom modules and modularity as descriptors in neural network models. Submitted Ago 2022.


