# Assignment #08: Clustering & PCA

## Reflection

In this assignment, we explored clustering techniques using the Forest Fire dataset and evaluated the effects of different preprocessing and dimensionality reduction methods on clustering outcomes. Our primary focus was on analyzing the impact of various scalers (StandardScaler, MinMaxScaler, and Normalizer) and applying Principal Component Analysis (PCA) to observe their influence on clustering algorithms, specifically k-Means, Agglomerative Clustering, and DBSCAN.

Initially, we cleaned and preprocessed the data by checking for missing values and encoding categorical features. We then scaled the data with three different scaling techniques. StandardScaler transformed features to have a mean of zero and unit variance, MinMaxScaler scaled features to a [0,1] range, and Normalizer scaled data points individually to unit norm. Each scaler provided unique results and influenced the clusters formed by the algorithms.


Using the the elbow method we determined the optimal number of clusters to be 3. We used 2 principal components. 

When performing K-means clustering we found that the Normalizer produced the highest silhouette score which meant a better defined cluster. For Agglomerate clustering, again Normalizer produced the highest silhouette score indicating a better defined cluster. In DBSCAN, MinMAXScaler performed the best as it was able to form clusters unlike StandardScaler and Normalizer. 

We discovered that, PCA with Agglomerate clustering clustering prodcued the best results when we combine PCA and other types of clustering. This was closely followed by PCA combined with K-Means.

On a whole, we discovered that K-Means clustering with the Normalizer produced the highest silhouette score indicating much better defined clusters.

Our key takeaway from this assignment is the importance of careful preprocessing and dimensionality reduction. The scaling method and the application of PCA significantly impact clustering outcomes, affecting both cluster separability and algorithm performance. This experience has helped us understand the intricacies of clustering analysis and the impact of different data manipulation techniques.

## Reflection Questions

### Humphrey Borketey

- **What do I believe I did well on this assignment?**
  I did well to perform some preprocessing on the dataset before the group began work on clustering. I worked on determining the optimal k using the elbow method and visualized the result. Addtionally, I setup the scalers, and performed K-means clustering, Agglomerate clustering, and interpretated the results for each. Having worked with the different scalers in the previous cross validation project, creating a pipeline to use for clustering went well.

- **What was the most challenging part of this assignment?**
  A challenge for me was understanding how to determine which clusters performed better. Although we had reviewed the elbow method and silhouette scores in class they seemed abstract. This exercise put it into a lot more perspective. The elbow method helped us determine the number of clusters to form while the silhouette scores helped in determine which of the clusters were better formed. This showed how the two techniques can be used together. Also, we had to refactor our solution and setup the notebook in a more readable way so we could easily determine the impacts of the various methodologies we used.

- **What would have made this assignment a better experience?**
  Some addtional in-class training on PCA would have been beneficial and how it impacts clustering results. Also, a lecture on the different scalers and knowing when to choose which given a particular dataset would be helpful.

- **What do I need help with?**
  I was able to understand clustering a lot better given the dataset. I believe given a larger more complex dataset,  techniques or issues to look for when performing clustering will be helpful.

### Uchechi Nwala

- **What do I believe I did well on this assignment?**
  I contributed significantly to the data preprocessing section, which is a critical foundation for this project. I ensured that the dataset was properly cleaned by addressing missing values, scaling numerical features, and encoding categorical variables effectively. My efforts allowed the team to focus on analysis and modeling without concerns about data inconsistencies or preprocessing errors. Additionally, I facilitated smooth collaboration by organizing the preprocessing pipeline in a clear and reusable manner, ensuring consistency across all subsequent analyses.

- **What was the most challenging part of this assignment?**
  The most challenging part of this assignment was determining the optimal number of clusters and principal components. Balancing these choices required understanding the trade-offs between simplicity and interpretability versus capturing the complexity of the data. For clustering, it was particularly difficult to decide the number of clusters due to differences in results across methods like the elbow method and silhouette analysis. For PCA, interpreting the explained variance and deciding how many components to retain while preserving meaningful data patterns presented another layer of difficulty. These challenges required not only technical skills but also judgment and iteration, which took significant time and effort.

- **What would have made this assignment a better experience?**
  Having a more comprehensive introduction to PCA and clustering methodologies at the start of the project would have been immensely helpful. For PCA, a hands-on tutorial or case study explaining the concepts of explained variance, eigenvalues, and eigenvectors would have clarified the theoretical underpinnings. Similarly, for clustering, examples comparing different techniques (e.g., K-Means, DBSCAN, and Agglomerative Clustering) on similar datasets would have made it easier to choose the right approach for our data. Overall, a stronger foundation in the application of these techniques would have improved our confidence and reduced the time spent figuring out the nuances during the assignment.

- **What do I need help with?**
  I would benefit greatly from more detailed examples on interpreting PCA results and clustering outcomes. For PCA, I’d like to better understand how to relate principal components back to the original features and how to identify which features contribute the most to each component. For clustering, more guidance on interpreting silhouette scores and determining the practical implications of cluster quality would be helpful. Additionally, examples of how to explain clustering results in the context of real-world scenarios would enhance my ability to communicate findings effectively. Access to similar solved problems or walkthroughs could also strengthen my ability to apply these techniques independently.

### Kiana Kiashemshaki

- **What do I believe I did well on this assignment?**
I used PCA to simplify the dataset while retaining its most significant features. Reducing the dataset to two dimensions allowed me to provide a clear structure for clustering methods, which worked effectively in this reduced space. K-Means and Agglomerative Clustering, in particular, benefited from this approach, as they produced well-separated and meaningful clusters.
In addition to applying PCA, I focused on making the clustering results visually accessible. I created interactive visualizations using Plotly for K-Means, Agglomerative Clustering, and DBSCAN. These plots allowed for an intuitive understanding of how clusters formed in the reduced space and made it easy to compare the performance of each method. My interpretation of the results added depth to the analysis. K-Means performed well by producing compact, spherical clusters, which is reflected in its strong silhouette score. Agglomerative Clustering outperformed K-Means slightly by better handling irregular cluster shapes, thanks to its hierarchical approach. DBSCAN, however, struggled with PCA-reduced data because its density-based assumptions didn’t align well with the transformed space.

- **What was the most challenging part of this assignment?**
The most challenging part of this project was analyzing the interaction between PCA and DBSCAN. While PCA simplified the dataset for algorithms like K-Means and Agglomerative Clustering, it altered the density structure of the data, making it difficult for DBSCAN to form meaningful clusters. This required significant experimentation with DBSCAN’s parameters, such as eps and min_samples, to better suit the transformed data. Another challenge was ensuring that the interactive visualizations captured the nuances of each clustering method while remaining clear and intuitive. Representing each cluster distinctly and making the visualizations engaging required careful consideration.

- **What would have made this assignment a better experience?**
This project could have been improved by exploring other dimensionality reduction techniques like t-SNE or UMAP, which might have aligned better with DBSCAN’s density-based approach. Having more examples or resources to explain the interaction between dimensionality reduction and density-based clustering would have been incredibly helpful. Experimenting with advanced clustering techniques, such as Gaussian Mixture Models or Spectral Clustering, could have also added depth to the analysis and potentially yielded better insights for more complex datasets.

- **What do I need help with?**
I would like to better understand how to systematically fine-tune DBSCAN’s parameters, particularly in cases where dimensionality reduction techniques like PCA are applied. Exploring other dimensionality reduction methods, such as t-SNE and UMAP, and their impact on clustering performance is another area I am eager to investigate. Additionally, I want to learn more about advanced clustering techniques and how to combine them with feature extraction methods like PCA to tackle even more complex datasets.






