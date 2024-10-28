# Counterfactual Explanations for Quantitative Bipolar Argumentation Frameworks (QBAFs)
[Effectiveness + acyclic]
(1) Run CFX_generate_binary_tree.ipynb to generate tree QBAFs of depth of 7.
just change depth = xxx to decide how deep of a tree QBAF you want.
no need to change N = 100, as this controls how many QBAFs you want to create.
(2) Run CFX_all_acyclic_QBAFs.ipynb to get the results. 
Change the following lines for the ablation studies:
        polarity = compute_polarity_vector(graph_dict, topic_arg, adj_matrix)
        priority = compute_priority_vector(graph_dict, topic_arg)
        # polarity = [0] * len(origin_base_score_dict)
        # priority = [1] * len(origin_base_score_dict)

[Effectiveness + cyclic]
(1) Run CFX_generate_QBAF_cyclic.ipynb to generate QBAFs of size 100.
just change num_nodes = xxx to decide how many number of nodes you want in a QBAF
no need to change N = 100, as this controls how many QBAFs you want to create.
(2) Run CFX_all_cyclic_QBAFs.ipynb to get the results. 
Change the following lines for the ablation studies:
        polarity = compute_polarity_vector(graph_dict, topic_arg, adj_matrix)
        priority = compute_priority_vector(graph_dict, topic_arg)
        # polarity = [0] * len(origin_base_score_dict)
        # priority = [1] * len(origin_base_score_dict)

[Scalability + acyclic]
(1) Run CFX_generate_binary_tree.ipynb to generate tree QBAFs of different size.
just change depth = xxx to decide how deep of a tree QBAF you want.
no need to change N = 100, as this controls how many QBAFs you want to create.
(2) Run CFX_all_acyclic_QBAFs.ipynb to get the results.
(3) Run CFX_plot_result to get the plots of scalability

[Scalability + cyclic]
(1) Run CFX_generate_QBAF_cyclic.ipynb to generate cyclic QBAFs of different size.
just change num_nodes = xxx to decide how many number of nodes you want in a QBAF
no need to change N = 100, as this controls how many QBAFs you want to create.
(2) Run CFX_all_cyclic_QBAFs.ipynb to get the results.
(3) Run CFX_plot_result to get the plots of scalability

[Robustness]
(1)Run CFX_generate_QBAF_cyclic.ipynb (or cyclic) to generate QBAFs of 100 arguments or depth of 7..
(2) Run CFX_all_robust_metric1_acyclic_QBAFs .ipynb to generate the reuslts.
Or  Run CFX_all_robust_metric2_acyclic_QBAFs .ipynb to generate the reuslts.
Or  Run CFX_all_robust_metric1_cyclic_QBAFs .ipynb to generate the reuslts.
Or  Run CFX_all_robust_metric2_cyclic_QBAFs .ipynb to generate the reuslts.
    change epsilon = 1e-1 to get different results.
(3) Run CFX_plot_result to get the plots of robustness.


(3) Run CFX_plot_result to get the plots of robustness


**File:** CFX_generate_QBAF_acyclic.ipynb  
**Input:** N: the number of QBAFs; num_nodes: the number of nodes in each QBAF; p: the probability of generating an edge between any two nodes.  
**Output:** N acyclic QBAF files named acyclic_{i}.bag  

**File:** CFX_generate_QBAF_cyclic.ipynb  
**Input:** N: the number of QBAFs; num_nodes: the number of nodes in each QBAF; p: the probability of generating an edge between any two nodes.  
**Output:** N cyclic QBAF files named cyclic_{i}.bag  

**File:** CFX_single_acyclic_QBAFs.ipynb  
**Input:** An acyclic QBAF file (xxx.bag).  
**Output:** A potential base score vector that makes the final strength of the topic argument as the desired strength.

**File:** CFX_single_cyclic_QBAFs.ipynb  
**Input:** A cyclic QBAF file (xxx.bag).  
**Output:** A potential base score vector that makes the final strength of the topic argument as the desired strength.

**File:** CFX_all_acyclic_QBAFs.ipynb  
**Input:** A number of acyclic QBAF files (xxx.bag).  
**Output:** The average/median metrics of the QBAFs, including validity, proximity, runtime.

**File:** CFX_all_cyclic_QBAFs.ipynb  
**Input:** A number of cyclic QBAF files (xxx.bag).  
**Output:** The average/median metrics of the QBAFs, including validity, proximity, runtime.


**File:** CFX_plot_resutl
**Instruction:** This file can plot the results in Figure 5 and 7.
