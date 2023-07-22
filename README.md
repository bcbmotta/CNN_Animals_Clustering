# CNN_Animals_Clustering
Applied Convolutional Neural Network to cluster animals images

- Used the pre-trained RESNET-50 model (with 23.5M parameters).
- Extracted the features from each image in a given dataset with 5000 animal images divided into 10 types of animal.
- Used K-Means to cluster the dataset into 10 groups, without giving the model the real labels.
- Compared the clusters with the real labels to understand if the model was able to correctly separate the animals.

## Results:

With an accuracy of 77.84%, we can consider that the model performed well in clustering the image database. Considering that the model was built based on an unsupervised machine learning algorithm, where it had no access to the real labels at any point during training, it was able to distinguish the 5000 images in the database very effectively and create 10 well-defined clusters, which were later compared to the true labels.

Analyzing the confusion matrix more deeply, we observe that the model had difficulty grouping the cow images into the same cluster, with this group showing the highest classification error. Two other groups that were not well identified were horses and sheep, although with fewer errors than cows. For all the remaining groups, the model achieved precision higher than 80%, reaching 96.6% in the case of butterflies, which can be considered an excellent result.

As we can see, just by using a pre-trained model without any further training, the unsupervised model showed good performance in image database clustering. One way to further improve this model would be to perform new training using the selected image database, as it is already labelled.
