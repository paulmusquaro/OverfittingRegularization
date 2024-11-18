# OverfittingRegularization

This project demonstrates how overfitting occurs in linear regression models and how regularization techniques can be applied to address it. It explores the concept of linear relationships between features and the target variable in a dataset and investigates the impact of collinearity, regularization, and feature scaling on model performance.


## Project Overview

In this project, we work with a dataset "bikes_rent.csv" which contains information about bike rentals and various weather and calendar features for different days. Our objective is to predict the number of bike rentals (cnt) based on these features. The dataset includes both continuous and categorical features like temperature, humidity, wind speed, and more.

### Key Components:
1. **Data Exploration**:
   - Loading and inspecting the dataset using `pandas`.
   - Analyzing the correlations between features and the target variable.
   - Visualizing dependencies between various features and the number of bike rentals.

2. **Correlation Analysis**:
   - Using Pearson correlation to assess the linear relationships between features and the target variable.
   - Identifying highly correlated features such as `temp` and `atemp`, and `windspeed(mph)` and `windspeed(ms)`.

3. **Feature Scaling**:
   - Standardizing the dataset using `scale` from `sklearn.preprocessing` to address features with different scales.
   - Shuffling the dataset to prepare it for training.

4. **Linear Regression Model**:
   - Training a linear regression model on the scaled data.
   - Analyzing the model's weights to identify potential issues with collinearity, which may result in large coefficients for highly correlated features.

5. **Overfitting & Regularization**:
   - Understanding overfitting caused by collinearity.
   - Exploring the application of L1 (Lasso) and L2 (Ridge) regularization techniques to mitigate overfitting and improve model generalization.


## Conda (Setup and Environment)

To make the project reproducible and ensure smooth package management, this project uses Conda as a package and environment manager. Below are the steps to set up the environment:


1. **Install Conda**:
If you haven't installed Conda yet, you can download it from the official [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) websites. Anaconda is a larger distribution with more pre-installed packages, while Miniconda is a smaller, minimal version. Choose whichever suits your needs.

2. **Create a new environment:** Open your terminal and run the following command to create a new Conda environment with Python 3.12:

    ```bash
    conda create --name new_conda_env python=3.12
    ```

3. **Activate the environment:** Once the environment is created, activate it by running:

    ```bash
    conda activate new_conda_env
    ```

4. **Install required packages (Jupyter, NumPy, MatPlotLib, Pandas and Scikit-Learn)**

    ```bash
    conda install jupyter numpy matplotlib pandas scikit-learn
    ```

5. **Run Jupyter Notebook**

    ```bash
    jupyter notebook
    ```

***
## Conclusion

This project demonstrates the importance of understanding overfitting and regularization in linear regression models. By analyzing the dataset, performing correlation checks, and applying feature scaling, we can build a more robust model. Regularization techniques such as Ridge and Lasso help address the challenges posed by multicollinearity, making the model more reliable and less prone to overfitting.