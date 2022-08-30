<h2 align="center">Network Analysis-Based Drug Repurposing for Glioblastoma</h2>

This [folder](https://github.com/ncats/drug_rep/tree/main/Glioblastoma_Subgraph) contains information related to the development and analysis of a glioblastoma-based network of rare disease data for the purpose of identifying potential candidates for drug repositioning to treat glioblastoma. 

<!---
mention NCATS GARD Knowledge graph here
-->

### Lab Notebook 

- **[Lab_Notebook.pdf](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Lab_Notebook.pdf)**: This file contains a link to a Google Document containing detailed notes taken throughout the duration of this project, including the Cypher commands used to extract subgraphs from the NCATS GARD knowledge graph, further detail on merging associated nodes, and Gephi metric reports for various iterations of GBN and mc_GBN. 



### Code files

- **[Create_Node_and_Edge_Lists.ipynb](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Create_Node_and_Edge_Lists.ipynb)**: This code takes JSON files containing the node and edge lists for each of the 92 glioblastoma-related subgraphs extracted from the NCATS GARD Knowledge Graph, converts them to CSVs, and appends them into a single node and single edge list.  

- **[Merge_Nodes.ipynb](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Merge_Nodes.ipynb)**: This code takes a list of graph nodes and a list of graph edges as input. It then merges (see documentation within file for details) all nodes connected by edges labeled “I_CODE”, “N_Name”, "R_exactMatch", "R_equivalentClass", and "PAYLOAD" and produces the modified node and edges lists as an output. 



### Data files 

- **[GBN_Node_List.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/GBN_Node_List.csv)**: A list of the 1,466 nodes contained in the GBN after associated nodes were merged via [Merge_Nodes.ipynb](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Merge_Nodes.ipynb). Can be used in conjunction with [GBN_Edge_List.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/GBN_Edge_List.csv) to reconstruct the GBN in a visualization tool (e.g. Gephi).

- **[GBN_Edge_List.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/GBN_Edge_List.csv)**: A list of the 107,423 edges contained in the GBN after associated nodes were merged via [Merge_Nodes.ipynb](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Merge_Nodes.ipynb). As edges are directed, each is denoted by a "Source" and "Target" node. Can be used in conjunction with [GBN_Node_List.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/GBN_Node_List.csv) to reconstruct the GBN in a visualization tool (e.g. Gephi).

- **[GBN_Centrality_Scores.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/GBN_centrality_scores.csv)**: A list of the degree centrality score, closeness centrality score, betweenness centrality score, eigenvector centrality score, and PageRank centrality score of each node within the GBN. 

- **[mc_GBN_Node_Modularity_Classes.csv](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/mc_GBN_Node_Modularity_Classes.csv)**: A list containing the nodes in mc_GBN and the modularity class each node has been assigned to.  

- **[mc_GBN_Node_Lists folder](https://github.com/ncats/drug_rep/tree/main/Glioblastoma_Subgraph/mc_GBN_Node_Lists)**: Each file within this folder contains the list of nodes for one mc_GBN (modularity class). This node list can be used in conjunction with its corresponding edge list from [mc_GBN_Edge_Lists folder] to reconstruct the mc_GBN in a visualization tool (e.g. Gephi). Node lists are included for all mc_GBN with more than three nodes.

- **[mc_GBN_Edge_Lists folder](https://github.com/ncats/drug_rep/tree/main/Glioblastoma_Subgraph/mc_GBN_Edge_Lists)**: Each file within this folder contains the list of edges for one mc_GBN (modularity class). This edge list can be used in conjunction with its corresponding node list from [mc_GBN_Node_Lists folder] to reconstruct the mc_GBN in a visualization tool (e.g. Gephi). Edge lists are included for all mc_GBN with more than three nodes.

- **[Modularity_Class_Centrality_Tables folder](https://github.com/ncats/drug_rep/tree/main/Glioblastoma_Subgraph/modularity_class_centrality_tables)**:



### Result files

- **[mc_GBN_Modularity_Class_Descriptions.pdf](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/mc_GBN_Modularity_Class_Descriptions.pdf)**: Brief descriptions of each of the forty-one modularity classes in mc_GBN.

- **Centrality_Score_Tables.pdf**: 

- **[Top_Candidate_Reference_List.xlsx](https://github.com/ncats/drug_rep/blob/main/Glioblastoma_Subgraph/Top_Candidate_Reference_List.xlsx)**: 