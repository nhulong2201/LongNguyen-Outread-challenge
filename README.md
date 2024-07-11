Please first download the <a href="https://drive.google.com/drive/folders/1Sbk_kYCn2vngGJ3cGSInMMZUqzfLMdnt?usp=sharing">datasets</a> and extract it in the same folder as the Jupyter notebook.

The following step is to run the code blocks in the Jupyter notebook sequentially.

My approach is as follows:

1. To extract the Abstract, for each PDF, I read in the first page and convert them to lowercase. I use the heuristic that the abstract is usually located between the 2 keywords "Abstract" and "Introduction".

2. Vectorization: I first removed all the stopwords and applied lemmatization. To vectorize text, I used Word2Vec as it captures the semantic and contextual information, while IT-IDF only captures the importance of the word based on frequency scores.

3. Clustering: I utilised DBSCAN to cluster the papers because it can handle nested clusters. In addition, it is more efficient to handle noises, compared to K-Means method.

4. To visualize, I use PCA to convert multi-dimensioned space into 2D space.

5. To evaluate the clustering quality, I calculated the average silhouette score. 
