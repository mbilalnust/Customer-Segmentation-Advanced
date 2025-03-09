# Clustering with LLM

## Introduction

In this project, I explore advanced techniques for customer segmentation through clustering. I've created this repository to share my journey in exploring different clustering approaches, which I believe will be valuable for data scientists looking to expand their toolbox and advance towards becoming senior data scientists.

### What I'll Cover

I explore three methods to approach customer segmentation projects:

1. Kmeans
2. K-Prototype
3. LLM + Kmeans

![Getting Started](img/com2d2.png)

I'll provide a comparison of 2D representations (PCA) of the different models I created. You'll also find my work with dimensionality reduction techniques such as PCA, t-SNE, and MCA, with results included.

![Getting Started](img/METH.png)

**Important Note**: In this project, I focus on the clustering methods rather than the exploratory data analysis (EDA) phase or variable selection, though these are crucial steps in such projects.

## Data

I'm using data from a public Kaggle dataset called "Banking Dataset - Marketing Targets." Each row contains information about a company's customers, including both numerical and categorical fields. I chose this dataset because its diversity in data types allows me to demonstrate various approaches to the problem.

I focus on the first 8 columns of the dataset, which include:

- `age` (numeric)
- `job`: type of job (categorical)
- `marital`: marital status (categorical)
- `education`: education level (categorical)
- `default`: has credit in default? (binary)
- `balance`: average yearly balance in euros (numeric)
- `housing`: has a housing loan? (binary)
- `loan`: has a personal loan? (binary)

I'm using the training dataset from Kaggle, which you can find in the "data" folder as a compressed file. Inside, you'll find two CSV files: `train.csv` (the original training dataset) and `embedding_train.csv` (the dataset after performing an embedding, which I'll explain later).

Here's how I've structured the project:

```
clustering_llm
├─ data
│  ├─ data.rar
├─ img
├─ embedding.ipynb
├─ embedding_creation.py
├─ kmeans.ipynb
├─ kprototypes.ipynb
├─ README.md
└─ requirements.txt

```

## Method 1: Kmeans

I start with Kmeans, a commonly used clustering method, where I demonstrate advanced analysis techniques. You can find my complete procedure in the Jupyter notebook titled `kmeans.ipynb`.

## Method 2: Kprototype
Here, I explore a method to create clusters when dealing with a mix of features (categorical and numerical). Check out my implementation in the Jupyter notebook titled `kprototypes.ipynb`.

## Method 3: LLM + Kmeans
This is my favorite part of the project, where I demonstrate how to apply LLM to obtain impressive results in clustering projects. You can find my approach in the Jupyter notebook titled `embedding.ipynb`.





