# Accident-Zone-Clustering
This project applies DBSCAN (Density-Based Spatial Clustering of Applications with Noise) to identify accident-prone zones based on spatial and contextual features. DBSCAN was selected over centroid-based methods to capture irregular cluster shapes better and to handle noise in real-world accident data.

Methodology
Input features were standardised before clustering.
DBSCAN parameters were tuned (eps = 0.5, min_samples = 20) to balance cluster separation and noise handling.
Noise points were explicitly identified and excluded from cluster count analysis.

Results
Clustering algorithm: DBSCAN
Silhouette Score: 0.882
Estimated number of clusters: Derived after excluding noise points
Noise points: Automatically detected by the algorithm. Noise points were excluded from Silhouette Score computation to evaluate cluster cohesion and separation only among core and border points identified by DBSCAN.
A high Silhouette Score indicates strong separation between accident-prone zones and well-defined cluster structure, supporting the effectiveness of density-based clustering for this problem.

Outcome
The clustering results highlight high-risk accident zones while filtering out isolated incidents as noise, enabling more reliable identification of areas requiring targeted intervention or further analysis.
Practical Use Case
The identified accident-prone zones can help new travellers and tourists recognise high-risk areas in advance. This supports better route planning, increased precaution, and informed decision-making, ultimately contributing to accident prevention and safer travel experiences.

Dataset:
The full original accident dataset is not included due to size constraints.
To demonstrate the workflow and results, a preprocessed subset (`accidents_final_states.csv`) containing only relevant features and filtered states is included. This dataset has gone through scaling, clustering, and state selection, and is provided to allow reproducibility of the pipeline and visualization steps.
The included dataset is a processed version for demonstration purposes only. The pipeline can be applied to the full dataset by replacing this file with the original `accidents_big.csv`.
