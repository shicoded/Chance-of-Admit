# Chance-of-Admit
This project aims to predict the chance of admission of students into graduate programs based on various features such as GRE score, TOEFL score, university rating, SOP, LOR, CGPA, research experience, etc. Using Decision Tree Regression, we aim to build a model that can accurately predict the likelihood of admission.

Decision Tree Regression - Scikit Learn

********
## Table of Contents
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Conclusion](#conclusion)
- [License](#license)
  
**********
## Dataset
The data set of graduate programshas in this repository above. you can download it and use.

**********
## Project Structure

- Decision Tree
  
A Decision Tree is a supervised machine learning algorithm used for classification and regression tasks. It models decisions in a tree-like structure, where each internal node represents a test or decision on a feature, each branch represents the outcome of the decision, and each leaf node represents a final prediction or output.

**How It Works:**

Root Node:

The tree starts with the root node at the top, which splits the data based on the CGPA value of 8.93. This split divides the data into two groups: those with a CGPA less than or equal to 8.93 and those with a CGPA greater than 8.93. The root node has 320 samples with an average predicted admission likelihood value of 0.731.
First Level of Splitting:

The left branch splits further based on a CGPA of 8.035. This suggests that students with a CGPA less than or equal to 8.035 are further evaluated based on their GRE score.
The right branch splits based on a CGPA of 9.225, indicating that students with a CGPA greater than 8.93 but less than or equal to 9.225 are evaluated further.
Second Level of Splitting:

On the left branch, the GRE score becomes the deciding factor for those with CGPA less than or equal to 8.035. If a student's GRE score is less than or equal to 305.5, the predicted likelihood of admission is lower (value = 0.514).
For students with a CGPA between 8.035 and 8.63, the likelihood of admission increases (value = 0.702) and further splits based on a CGPA of 8.63.
On the right branch, students with a CGPA between 9.225 and 9.465 have a higher likelihood of admission, and the tree further splits based on their GRE score or CGPA.
Leaf Nodes:

The leaf nodes at the bottom of the tree represent final predictions for the likelihood of admission. These nodes do not split further and provide the predicted value (e.g., 0.514, 0.836, 0.953, etc.), which indicates the model's prediction for admission likelihood based on the paths taken through the tree.

`Decision Paths:` To make a prediction, the model starts at the root node and follows the decision paths according to the values of the input features until it reaches a leaf node.

**Example:**

Imagine you want to predict whether a student will be admitted to a graduate program. The Decision Tree might first split the data based on GRE scores. If a student's GRE score is above a certain threshold, the tree might then consider the student's CGPA. Depending on these features and others like research experience, the tree ultimately arrives at a decision, such as "Admitted" or "Not Admitted."

**Advantages:**

Easy to Understand: The tree-like structure is intuitive and can be easily visualized.
Non-linear Relationships: Decision Trees can capture non-linear relationships between features and the target variable.

**Limitations:**

Overfitting: Trees can become overly complex and overfit the data, especially if not pruned or regularized.
Instability: Small changes in the data can result in a completely different tree structure.

***********

Squared Error:

Each node also provides a "squared_error" value, which represents the mean squared error (MSE) for the samples in that node. Lower squared errors indicate more precise predictions.
Summary:
This Decision Tree model uses CGPA and GRE scores to predict the likelihood of student admission. The tree first evaluates CGPA and then further splits based on GRE scores or refined CGPA values, leading to a final prediction at the leaf nodes. The model shows how different combinations of these features can impact the likelihood of a student's admission into a graduate program.





