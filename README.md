# Customer Segmentation Using Advanced Clustering Techniques

## 📋 Overview
This project explores innovative approaches to customer segmentation using a combination of traditional clustering methods and modern Language Models (LLM). It's designed to showcase how advanced techniques can enhance customer segmentation beyond conventional methods.

### 🎯 Project Goals
- Demonstrate advanced customer segmentation techniques
- Compare traditional and LLM-based clustering approaches
- Provide practical insights for data scientists looking to expand their toolbox

## 📊 Data Description

### Dataset Source
The analysis uses the "Banking Dataset - Marketing Targets" from Kaggle, chosen specifically for its diverse mix of data types that allows demonstration of various clustering approaches.

### Key Features
The analysis focuses on 8 primary customer attributes:
- `age` (numeric): Customer's age
- `job` (categorical): Type of occupation
- `marital` (categorical): Marital status
- `education` (categorical): Education level
- `default` (binary): Credit default status
- `balance` (numeric): Average yearly balance in euros
- `housing` (binary): Housing loan status
- `loan` (binary): Personal loan status

### Data Files
Located in the `data` folder:
- `train.csv`: Original training dataset
- `embedding_train.csv`: Processed dataset with embeddings

## 🗂️ Project Structure
```
clustering_llm
├─ data/
│  └─ data.rar
├─ img/
├─ kmeans_llm.ipynb          # LLM-based clustering implementation
├─ llm_embedding.py    # Embedding generation script
├─ kmeans.ipynb            # Traditional clustering implementation
├─ kprototypes.ipynb       # Additional clustering experiments
├─ README.md
└─ requirements.txt
```

## 🔍 Methodology

### Method 1: Enhanced K-means Approach
This approach combines unsupervised and supervised learning for a comprehensive segmentation solution.

#### Components
1. **K-means Clustering (Unsupervised)**
   - Creates initial customer segments
   - Identifies natural patterns without predefined labels
   - Groups customers based on feature similarity

2. **LightGBM Classifier (Supervised)**
   - Interprets clustering results
   - Explains cluster assignments
   - Provides feature importance via SHAP values

#### Key Benefits
- Combines discovery (K-means) with interpretation (LightGBM)
- Answers both "what" and "why" questions about segments
- Provides actionable insights for business decisions

### Method 2: LLM-Enhanced Clustering
This innovative approach leverages the power of Language Models to create more nuanced customer segments.

#### Process Flow
1. **Text Transformation**
   - Converts customer data into structured text descriptions
   - Standardizes mixed data types into a unified format
   - Example: "Age: 35, Job: engineer, Marital: married..."

2. **Embedding Generation**
   - Uses `paraphrase-MiniLM-L6-v2` transformer model
   - Creates high-dimensional vector representations
   - Captures semantic relationships between features

3. **Clustering Analysis**
   - Applies K-means to the embeddings
   - Groups customers in the semantic space
   - Identifies natural segments based on overall similarity

#### Advantages
1. **Data Handling**
   - Seamlessly processes mixed data types
   - Eliminates need for separate preprocessing
   - Maintains feature relationships

2. **Model Benefits**
   - Captures complex feature interactions
   - More robust to outliers
   - Leverages pre-trained language understanding

3. **Practical Benefits**
   - Simplified pipeline
   - More intuitive feature representation
   - Better handling of categorical relationships

## 📈 Results
The project includes visualizations and comparisons using:
- PCA (Principal Component Analysis)
- t-SNE
- MCA (Multiple Correspondence Analysis)

Detailed results and comparisons can be found in the respective notebooks.

## 🚀 Getting Started
1. Clone the repository
2. Extract the data from `data/data.rar`
3. Install requirements: `pip install -r requirements.txt`
4. Explore the notebooks in order:
   - `kmeans.ipynb` for traditional approach
   - `embedding.ipynb` for LLM-based approach

## 📝 Note
This project focuses on clustering methodologies rather than extensive EDA or feature selection. For production applications, consider incorporating these additional steps into your pipeline.
