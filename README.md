# hdsvm

`hdsvm` is an R package for high-dimensional support vector machines. It is especially useful for classification problems where the number of features is much larger than the number of samples, such as in gene expression datasets.

This README shows basic usage examples based on the official [vignette](https://cran.r-project.org/web/packages/hdsvm/vignettes/hdsvm-vignette.html).

## Introduction
This package provides tools for fitting the penalized SVM.

The strengths and improvements that this package offers relative to other SVM packages are as follows:

- Compiled Fortran code significantly speeds up the penalized SVM estimation process.

- Solve the elastic net penalized SVM using generalized coordinate descent algorithm.

- Active-set and warm-start strategies implemented to compute the solution path as $\lambda_1$ varies.

Then the penalized SVM model is formulated as:

![penalized SVM](https://latex.codecogs.com/svg.image?\dpi{130}&space;\min_{\beta\in\mathbb{R}^p,\;b_0\in\mathbb{R}}&space;\frac{1}{n}&space;\sum_{i=1}^n&space;\left[\max\left(1&space;-&space;y_i&space;(\beta_0&space;&plus;&space;x_i^\top&space;\beta),&space;0\right)\right]&space;&plus;&space;\lambda_1&space;\left\|pf_1&space;\circ&space;\beta\right\|_1&space;&plus;&space;\frac{1}{2}&space;\lambda_2&space;\left\|\beta\right\|_2)

where the ∘ symbol represents the Hadamard (element-wise) product.


## 📦 Installation

```r
install.packages("hdsvm")
