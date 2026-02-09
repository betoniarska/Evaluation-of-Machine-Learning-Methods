This exercise evaluates the spatial prediction performance of a 9-nearest neighbor regression (9NN) model for predicting water permeability. 
The goal is to assess how prediction performance changes as the spatial distance between training and test locations increases, using spatial 
leave-one-out cross-validation (SKCV) and the C-index performance metric.

The analysis uses three datasets, each containing 1690 data points:

input.csv | Contains 75 predictor variables for each observation. (All predictor variables are standardized using Z-score normalization prior to modeling.)
output.csv | Contains the target variable: water permeability.
coordinates.csv | Contains the spatial coordinates (x, y) of each observation, measured in meters.

All datasets are assumed to be aligned row-wise, meaning each row corresponds to the same spatial location across files.

SKCV

1. Each data point is treated as a test location once.
2. A spatial buffer distance d is applied, excluding all training points within d meters of the test point.
3. From the remaining points, the 9 nearest spatial neighbors are selected.
4. A 9NN regression model is trained using these neighbors.
5. The model predicts the target value at the test location.
6. Predictions across all valid test points are aggregated.
7. Model performance is evaluated using the C-index.

Results of the performance metric (C-index) are plotted for better visualization and analysis of the method
