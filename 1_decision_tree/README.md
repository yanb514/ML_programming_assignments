# Decision tree
The decision tree algorithm takes in a node class, which contains training data as an argument. `TreeGrowth` recursively finds the optimal split between the dataset according to either weighted Gini index or entropy ratio. In each recursive step, the two subsets from the best split are then assigned as the children to that node.

#### Data
The data can be found in the folder "cancer_datasets_v2"

#### Pseudocode and helper functions:
Please see the pdf attachment "HW1 binary decision tree.pdf"

#### Execute the code
Simply run Binary decision tree-submitted.ipynb in order

#### The best pruned tree
![treeplot](https://github.com/yanb514/ML_programming_assignments/blob/master/1_decision_tree/udo.png)
