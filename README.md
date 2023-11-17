# Classifying Violations in Labor Protection and Industrial Safety



***STATUS:*** **Completed**


## Shortly about the project:

Due to high security measures at the company, i can only share development details without delving into them, and i won't be able to demonstrate the source code.

Main goal was creating an algorithm for classifying violations in labor protection and industrial safety. A dataset of violations was provided, consisting of 17,841 rows with a text column describing the violations. The project aimed to showcase the most frequently occurring violations by workshops and on an annual basis. To implement this idea, i proposed the concept of classifying violations. After analyzing a portion of the violations, i developed 12 class options. Subsequently, in collaboration with the manager and senior audit manager, we refined some classes, resulting in a final set of 8 options. A decision was then made to label approximately 3,000 rows. After labeling 2,788 rows, i effortlessly built a predictive model for the remaining 15,053 rows.

To achieve this, i utilized the SpaCy language library to transform each word in the violation column into its base form and removed stopwords (e.g., he, my, means, to, between). Following that, considering the task's specificity, i selected the Random Forest algorithm for training (i won't describe the algorithm's operation). Hyperparameters were tuned using the RandomizedSearchCV component from the sklearn library. The chosen hyperparameters for the component were as follows: Estimators - 20, Maximum Depth - 19.

Subsequently, the model was trained on the provided parameters, and missing values were replaced with predicted classes with a training set accuracy of 0.89. After verifying functionality, the algorithm was refined by enriching the training and test sets with values that were predicted less accurately. The algorithm was presented at a meeting on occupational safety and industrial safety audit, as part of introducing a dashboard (also developed by me) for continuous auditing of accidents and compliance checks.

Later, the algorithm's results were integrated into the internal ACSiPB system for further updating the violation database and their classifications.

## Project Tools

- Python
- Pandas
- SpaCy
- Sklearn
