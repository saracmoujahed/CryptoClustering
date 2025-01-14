# CryptoClustering
# Cryptocurrency Clustering and PCA Analysis

## Overview
This program involves clustering cryptocurrencies based on their features using the K-Means algorithm and optimizing the clusters with Principal Component Analysis. The key steps include scaling data, determining the best value of k, clustering data, and analyzing feature influences on components.

### 1. Prepare the Data
- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
- Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
- Verify that the first five rows of the scaled DataFrame match the expected structure.

### 2. Find the Best Value for k Using the Original Scaled Data
- Use the elbow method to identify the optimal value for k.
  - Create a list of k values from 1 to 11.
  - Create an empty list to store the inertia values.
  - Use a for loop to compute the inertia for each value of k.
  - Create a dictionary with the data to plot the elbow curve.
  - Plot a line chart of inertia values to visually identify the best k.
- Answer: What is the best value for k?

### 3. Cluster Cryptocurrencies with K-Means Using the Original Scaled Data
- Perform clustering using the best value of k.
  - Initialize the K-Means model with the best value of k.
  - Fit the model using the scaled DataFrame.
  - Predict clusters and add the predicted clusters as a new column in a copy of the original DataFrame.
  - Create a scatter plot with:
    - x-axis: price_change_percentage_24h
    - y-axis: price_change_percentage_7d

### 4. Optimize Clusters with Principal Component Analysis
- Perform PCA on the scaled DataFrame to reduce features to three principal components.
  - Create a PCA model instance with n_components=3.
  - Transform the scaled data and create a DataFrame with the PCA data.
  - Retrieve the explained variance and determine the total explained variance for the three components.
- Answer: What is the total explained variance?

### 5. Find the Best Value for k Using the PCA Data
- Use the elbow method to determine the optimal value for k.
  - Repeat the steps for finding the best value for k using the PCA data.
  - Plot a line chart of inertia values for k values from 1 to 11.
- Answer:
  - What is the best value for k using PCA data?
  - Does it differ from the best k value found with the original data?

### 6. Cluster Cryptocurrencies with K-Means Using the PCA Data
- Perform clustering using the PCA data and the best value of k.
  - Initialize the K-Means model and fit it using the PCA data.
  - Predict clusters and add the predicted clusters as a new column in a copy of the PCA DataFrame.
  - Create a scatter plot with:
    - x-axis: PC1
    - y-axis: PC2
- Answer: What is the impact of using fewer features to cluster the data?

### 7. Determine the Weights of Each Feature on Each Principal Component
- Create a DataFrame showing the weights of each feature for each principal component using the columns from the original scaled DataFrame as the index.
- Answer: Which features have the strongest positive or negative influence on each component?

---

## How to Download and Use the Program

1. **Download the Repository**:
   - Clone the repository using the following command:
     ```bash
     git clone <repository_url>
     ```
   - Alternatively, download the ZIP file from the repository page and extract it to your desired directory.

2. **Set Up the Environment**:
   - Ensure Python is installed (Python 3.7 or higher is recommended).
   - Install the required libraries by running:
     ```bash
     pip install -r requirements.txt
     ```

3. **Prepare the Data**:
   - Place the cryptocurrency dataset CSV file in the project directory.
   - Update the file path in the Jupyter notebook if necessary.

4. **Run the Program**:
   - Open the Jupyter notebook:
     ```bash
     jupyter notebook
     ```
   - Navigate to the project directory and open the notebook file.
   - Execute the cells step-by-step to perform data scaling, clustering, PCA, and analysis.

5. **Analyze Outputs**:
   - Review the plots generated for the elbow method and clustering.
   - Examine the explained variance and feature weights to draw insights from the data.


## Deliverables
- Python code and outputs in a Jupyter notebook.
- Plots for the elbow method and cluster visualizations.
- Answers to the provided questions in your notebook.
