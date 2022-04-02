The dataset consists of 1M records of screening mammograms and the resulting diagnosis.
1. It has **imbalanced classes** ~ only **0.73%** records out of 1M are for positive cancer cases.
2. Features have missing values.


PROCESS:
1. data_preration.ipynb (COMPLETED)
   - Expand the aggregated dataset
   - Replace the missing values (represented by '9') with 'np.NaN' 
2. ds_process.ipynb (WIP)
   - Perform EDA, split data into test and train sets
   - use cross-validation, hyperparameter optimization
   - Make predictions
   - Choose Model with the 'best' performance

MODEL PERFORMACE:
1. Due to high class imbalance, accuracy is not an accurate measure of model performace.
2. Also successfully predicting cancer cases is more important than predicting non-cancer cases.
3. Hence Precision, Recall and F1-score are better measures of model performance. 
4. Using a precision-recall curve would be beter than ROC curve as it focuses the performace on the minority class.

MINIMIZE BUSINESS COSTS:
1. The cost of a False Negaative (cancer predicted as non-cancer) would be higher than a False Positive (non-cancer predicted as cancer)
2. According to an article on breast cancer misdiagnoses, the lifetime burden of False Positives is 2x the burden of False Negatives.
3. So we can create a cost funtion and choose a model which minimizes the cost function. For us this means, we will err on the side of caution, we will catch more cancer cases at the expense of of misclassifying some non-cancer cases as cancer. 





The dataset is sourced from https://www.bcsc-research.org/data/rfdataset
