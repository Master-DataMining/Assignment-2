# Assignment-2

# Goal

Perform different dimensionality reduction techniques on the image dataset and the tabular dataset

# PCA

Choose a color image and convert it into the black and white (grescale) image.

Perform PCA on the matrix with all the components.

Visualize how many components we could retain and how much cumulative variance they capture.

Pick a suitable number of components to represent the image for compression.

Reconstruct the image using 136 components and reconstruct image

Steps to reconstruct image:

*   Use the fit_transform method from the IncrementalPCA module
*   Find the 136 Principal components and transform and represent the data in those 136 new components/columns.
*   Reconstruct the original matrix from these 136 components using the inverse_transform method.
*   Plot the image to visually assess the quality of it.

The image looks much better but on a smaller resolution, it is not easy to detect the differences from the original greyscale image very easily. Therefore, reconstruct and plot for different number of components.

Plot the image and compare the differences

# SVD 

Use numpy.linalg for importing svd

Compressing and display the reconstructed images and display a plot of singular values

Create an interactive widget to explore how the quality of the reconstructed image varies with k.

SVD shows how the reconstructed image quality varies with different values of K. 

As we increase or decrease the k with the slider, the quality increases or decreases.

# tSNE

tSNE try to reduce dimension by preserving the neighborhood.

If we are taking a point a, in the original dimension (50 Features) and my closest neighbors were b,c,d,e,f. In the lower dimension also my closest neghbors should be b,c,d,e,f.

Measure the simmilarity between the neighbors by KL Divergence.

Compare the PCA and tSNE in MNIST and notice that the clusters are more clear for tSNE compared to PCA

# UMAP

UMAP outperformed t-SNE and PCA. 

The clusters are separated very well. For visualization purpose, UMAP shows the clusters, data points and the proximities in a very effective manner. 

The mini clusters are separated very well. 

UMAP is much faster than t-SNE. With latter the problem is that it needs another dimensionality reduction method to perform well otherwise it takes a longe time to compute.

# LLE

LLE performance was best among all the techniques. 

The computation time is less and also it provides the well- separated clusters that we were expecting.

Consideration of the non-linearity of the structure LLE goes beyond density modeling techniques such as local PCA.

Density models do not provide a consistent set of global coordinates which embed the observations across the entire manifold; thus they cannot be used.Methods like Kernel PCA, Isomap are also unable to detect the features which are detected by LLE.

# ISOMAP

Isomap performed  better than PCA.

Instead of measuring distance in pure Euclidean distance with the Pythagorean theorem, Isomap optimizes distances along a discovered manifold.
