# Investigating-the-impact-of-Training-Data-Selection-on-Calibration-and-Selective-Prediction

Given is a training dataset and its Data Map which tells us the distribution of training instances based on the model's predictions (i.e. which instances are easy and which ones are hard). Study the impact of Training data selection (from various regions of the Data Map) on model calibration and Selective Prediction performance in both In-Distribution Generalization and Out-Of-Distribution Generalization settings.



Datasets Used
  -  SNLI
https://nlp.stanford.edu/projects/snli/
  -  SWAG
https://arxiv.org/abs/1808.05326
  -  Commonsense QA
https://www.tau-nlp.org/commonsenseqa
  -  Abductive NLI
https://arxiv.org/abs/1908.05739
  -  Social IQA
https://leaderboard.allenai.org/socialiqa/submissions/get-started



### Data Mapping:
The Data Maps file serves the purpose of generating maps for each dataset by assuming the presence of a standardized file system to navigate through. During the data mapping process, it also creates graphs illustrating the distribution of average confidence, providing insights into the dataset's characteristics.

### Accuracy Calculation:
The Accuracy file is designed for calculating accuracy and selective prediction performance across different datasets. It utilizes global variables located at the file's beginning to specify dataset details, label count, and total epochs for each calculation. The execution assumes a standardized folder structure. Users have the flexibility to set the starting epoch for comparing accuracy and selective prediction performance. By adjusting the global variable, users can obtain performance readouts across all epochs or focus solely on the last epoch by setting the EPOCH_START variable equal to the model's total epochs.
