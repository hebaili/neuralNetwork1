# neuralNetwork1
This neural network contains 4 layers in total and 6 nodes in each hidden layer. The input layer has dim(X) of nodes, which is 6 when n=4, 10 when n=5 and 15 when n=6. The forward function shows how the data are processed. Data is linearly transformed into the first hidden layer. For the first three layers, I performed ReLU on hidden data via weights and linearly transform to the next hidden layer. I’ll be using sigmoid as the final layer so that we can get an output between 0 and 1.

I used cross entropy loss as the loss function because it is a classification problem. When writing the fit function to train the weights, X (data) and Y (target) are trained in 10000 iterations. Updating weights is done by back propagation and gradient descent.

For prediction and see how accurate the predictions are, predict (with a helper function, predict_proba) and score are added. Predict gives a result of either 1 or 0. Score gives the proportion of times when we are correct.

When training the data, I considered using cross-validation. However, I found the runtime will be extremely high when n = 6 due to relatively larger size of dataset and the result does not improve significantly. Therefore, I gave up cross-validation.
