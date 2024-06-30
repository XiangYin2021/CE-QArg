# Counterfactual-Argumentative-Explanations

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
This file can plot the results in Figure 5 and 7.
