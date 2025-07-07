# Implementing a Decision tree for decision-making

This project consists of the following tasks:
1. Implement a decision tree learning algorithm from scratch
Implement a greedy algorithm for learning decision trees:

* If all data points have the same label

...*return a leaf with that label
  
* Else if all data points have identical feature values

...* return a leaf with the most common label
  
• Else

  -choose a feature that maximizes the information gain
  
  -split the data based on the value of the feature and add a branch for each subset of data
  
  -for each branch
    ∗ call the algorithm recursively for the data points belonging to the particular branch

You should use entropy as the impurity measure. Your implementation should have two functions that the users can use:
1) learn(X, y, impurity_measure=’entropy’)
2) predict(x, tree)

2. Add Gini index
Implement Gini index as an alternative impurity measure. To use the Gini index, you should call your learning function like learn(X, y, impurity_measure=’gini’).

3. Add reduced-error pruning: Decision tree learning is prone to overfit. To fix this, extend your algorithm to tackle overfitting using reduced-error pruning:
  • Divide data to training and pruning (validation) data
  1) Use the training data to build a full decision tree T∗ (using the algorithm from Section 1.1)
  2) For each subtree T of T∗
    • If replacing the subtree with the majority label in T (based on training data) does not decrease accuracy on the pruning data
      -Replace T with a leaf node that predicts the majority class

4. Evaluate your algorithm
Load the Banknote Authentication dataset from MittUiB; alternatively, you can use https://archive.ics.uci.edu/ml/datasets/banknote+authentication. The task is to predict whether a banknote is genuine or fake. The first four columns of the data are continuous features extracted from images of the banknotes. The fifth column is the class label (1: genuine, 0: fake).

5. Compare your implementation to some existing decision tree implementation. How does your implementation fare against this implementation in terms of accuracy and speed? Can you explain the (possible) differences?
Note: You can compare to, for example, DecisionTreeClassifier from sklearn



This project contains the following files:

1. classes.py
2. decision_tree.py
3. feature_selection.py
4. impurities.py
5. main.py


In order to run the whole algorithm, it is enough to run the main.py file, while having all the files and also the data file downloaded in the same directory.



