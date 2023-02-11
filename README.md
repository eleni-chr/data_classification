# data_classification
Various functions for data classification.

Functions written by Eleni Christoforidou in MATLAB R2022b.

*my_fitpca*: This function takes as input the [MxN] data matrix D, containing N feature measurements for M samples, and the known classification for each sample in the [Mx1] vector called class. The function outputs the struct mdl, which contains the pca models created for each unique classification in class.

*MahalanobisDistance*: This function takes as input a single class from the pca model mdl and a [1xN] feature vector v, containing N feature measurements for a sample. It outputs the Mahalanobis distance from the feature vector to the pca model. It also outputs b, the coordinates within the pca model space for the feature vector, and std_per_mode, which contains the standard deviation distances from the mean for each mode of variation in the pca model.

*my_predictpca*: This function takes as input a pca model mdl and an [MxN] data matrix D, containing N feature measurements for M samples. It has two outputs, the classification for each sample in the [Mx1] vector class that is estimated using the pca model, and the Mahalanobis distance score for each sample in the [Mx1] vector score as the second output.
