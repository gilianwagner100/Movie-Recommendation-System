# Movie-Recommendation-System

## Overview
In our Master's degree "Business Analytics" at Nova School of Business and Economics, we, a team of 5 students, worked on a group project for the course "Machine Learning". Our objective was to develop a movie recommendation system using a dataset from Kaggle (https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/code?datasetId=3405&sortBy=voteCount) that contains movie ratings. Recommendation systems are highly relevant nowadays as they play a crucial role in enhancing user experience and engagement across various digital platforms. By providing personalized suggestions, recommendation systems help users discover content, products, or services that align with their preferences and interests, thereby increasing satisfaction and retention. In e-commerce, streaming services, social media, and many other domains, these systems drive significant business value by boosting sales, improving customer loyalty, and optimizing the overall interaction between users and the platform.

The project was divided into two parts: using traditional Machine Learning techniques in the first part and improving our recommendation system with Deep Learning techniques in the second part. After trying several models, we combined Content-Based as well as Collaborative Filtering techniques to maximize the relevance of our movie suggestions:
- Content-Based Recommender Systems allow for immediate personalization as we do not require ratings to start generating movie recommendations. This makes them very robust and allows for mitigation of the cold start problem. In the end, we combined **Word2Vec text embeddings with BERT-based sentiment analysis** which achieved a **precision of 80.74%**, meaning that in 10 suggested movies, at least 8 are relevant for the respective user.
- On top of that, a Collaborative Filtering model leverages user behavior and interactions to suggest movies that similar users have liked, enhancing personalization and relevance. Here, we are using a **Neural Collaborative Filtering (NCF)** model which combines Generalized Matrix Factorization and Multi Layer Perceptron to learn highly complex user-item interactions. This model achieved a **precision of 98.39%** and an **RMSE of 1.05** (on a rating scale of 0.5 to 5).

[Content Based Models - Overview](graphs/Content_Based_Models_Overview.png)

[Collaboreative Filtering Models - Overview](graphs/Collaborative_Filtering_Models_Overview.png)

## Repository Structure
**data:**
The directory where the data files from Kaggle should be placed.

**notebooks:**
This includes the Master Notebooks from both parts of the project.

## Usage
**Installation:**
1. Clone the repository:
```sh
    git clone https://github.com/gilianwagner100/Movie-Recommendation-System.git
    cd Movie-Recommendation-System
```
2. Install the required libraries:
```sh
    pip install -r requirements.txt
```
3. Download the dataset from Kaggle and place it in the `data/` directory.

**Running the Notebooks:**
1. Open Jupyter Notebook:
```sh
jupyter notebook
```

2. Run the notebooks `Part1_Master_Notebook.ipynb` and `Part1_Master_Notebook.ipynb` to see the implementation and results of the project.

## About
Students that developed this project:
- Gilian Wagner
- Leonardo Heinemann
- Malte Haupt
- Maximilian Schön
- Benedikt Tremmel