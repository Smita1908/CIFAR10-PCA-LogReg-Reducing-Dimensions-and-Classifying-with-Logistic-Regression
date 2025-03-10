# Principal Component Analysis for dimensionality reduction and visualization

# 🗣️Description: 
- This project deals with neural image classification using `PyTorch`.
  -  Unveiling patterns with PCA, visualizing Principal Components and navigating Image Classification with Logistic Regression
  -  Principal component analysis (PCA) is a technique used to emphasize variation and bring out strong patterns in a dataset.
  -  It's often used to make data easy to explore and visualize. PCA is also a very useful dimesnionality reduction technique.
  -  Here it is explored how to apply PCA on the CIFAR dataset for dimensionality reduction and visualization of principle component.
  -  Logistic regression is a classification algorithm used to assign observations to a discrete set of classes.
  -  Unlike linear regression which outputs continuous number values, logistic regression transforms its output using the logistic sigmoid function to return a probability value which can then be mapped to two or more discrete classes.

- 💡 Goal: Project high dimensional data to a specific low dimensional space. 

- 📊 Dataset: `CIFAR 10` - an inbuilt torchvision dataset

- 📚 Labels: 10 different classes ('plane', 'car', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck)

- 📄 Input Dimension: 3072(3* 32* 32)

- 📤 Output dimension: 50

- 🪜 Steps:
  - Transformation is done by centering and normalizing the images
  - Transformed matrix(data matrix) is of shape [No of images, 3072]
  - Covariance matrix is computed  of the data matrix by multiplying it with the transposed form
  - Eigenvectors and eigenvalues of the covariance matrix is computed by torch.eig function
  - Eigenvectors are sorted by decreasing eigenvalues
  - Top target_dim eigenvectors is selected to get the encoding matrix of shape [target_dim(50), dimensions]
  - Data matrix is multiplied with the encoding matrix to project the data into the low dimensional space
- 🖼️ Visualization
  - PCA is often used for visualization purposes.
    - Visually exploring the data can become challenging when we have more than 3 features.
      - A very useful tool when dealing with data related problems
      - Input : 3072 dimensions
      - Output: 2 dimensions
    - Plotting the data
      - For each data point, plot the first principle component on x  axis
      - The second principle component on y axis
      - use different colors for each class.
      - Set corresponding labels: assign label "first principle component" for x and y axis
      - Add legends for each class.

## 🚀How to run the project:
* There is a single jupyter file.
* Open the file using google colab or VScode.
* The file contains both the implementation of PCA(dimensionality reduction & visualization)  and the Logistic Regression classifer.
* The file contains detailed clear description of each step performed and packages to install(if any).

