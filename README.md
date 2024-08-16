# **Intrusion Detection Using Machine Learning Techniques On CIC-IDS2017 Dataset**

Created By [Mohammad Amirifard](https://www.linkedin.com/in/mohammad-amirifard/)


<img src="https://www.teligentsolutions.com/wp-content/uploads/2015/04/Teligent_Solutions_Intrusion_Detection.jpg" alt="Image" />

# **Problem Statement:**
The objective of this project is to **detect** and classify various types of **anomalies** within the `CIC-IDS2017 dataset`, which is a widely recognized benchmark dataset used for cybersecurity research, particularly in the domain of intrusion detection systems (IDS). Anomalies in this context refer to unusual or suspicious patterns in the network traffic data that may indicate potential security threats such as attacks or intrusions.

To achieve this, we will apply a range of **machine learning techniques** that are commonly used for anomaly detection and classification tasks. These techniques include, but are not limited to, supervised learning methods, such as decision trees, support vector machines, and neural networks, as well as unsupervised learning approaches like clustering algorithms and autoencoders. By leveraging these methods, we aim to accurately classify network traffic data into normal and anomalous categories.

The problem we are addressing is inherently a classification problem, where the primary goal is to categorize the data into predefined classes based on the learned patterns. This involves training machine learning models on labeled data to distinguish between normal and anomalous network traffic, enabling the detection of potential security threats with high precision and recall.

# **Goal:**

Our ultimate aim is to develop a robust system that can effectively identify various types of anomalies, contributing to the enhancement of network security measures.

# **Dataset:**
you can see detail of available dataset on this [link](https://www.unb.ca/cic/datasets/ids-2017.html)

# Rpository Structure:
```
- 📦 ....
  |- 📄 README.md        #Guide file
  |- 📄 License.md      #License file
  |- 📂 Data             #Here you can see dataset link.
  |- 📂 Notebooks        #Here you can see jupyter files which should be run on Google Colab or Kaggle.
  |- 📂 Src              #Here you can see python files to run
  |- 📂 Report           #Here you can see a complete report of what we have done.
```

# **Structure of notebooks**
`This program includes several notebooks regarding different parts.

1.   Notebook number 1, [Part1_EDA](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part1_EDA.ipynb)
2.   Notebook number 2, [Part2_KNN_Models](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part2_KNN_Models.ipynb)
3.   Notebook number 3, [Part3_SVM_Models](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part3_SVM_Models.ipynb)
4.   Notebook number 4, [Part4_Gboost_Model](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part4_GBoost_Model.ipynb)
5.   Notebook number 5, [Part5_MLP_Model](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part5_MLP_Model.ipynb)
6.   Notebook number 6, [Part6_Conclusion]()


# **Guide to run:**
# Option 1: Run it locally.For this, copy and paste the following commands in terminal of your IDE.
Step 1: 
```
git clone https://github.com/Mohammad-Amirifard/Intrusion_Detection.git
```
Step 2:
```
cd .\Intrusion_Detection\
```
 
Step 3:
```
pip install -r .\requirement.txt
```
Step 4: 
```
jupyter notebook
```
Step 5: Run each file you need. There is no necessity to run them in order.

# Option 2: Run files of Notebooks folder on Colab or Kaggle. There is no necessity to run them in order.


# Result

This analysis evaluates various machine learning models applied to anomaly detection tasks across multiple classes. The models were assessed using three primary metrics: **Weighted F1 Score**, **Macro F1 Score**, and **Accuracy**. These metrics provide a comprehensive understanding of each model's performance, particularly in handling class imbalances and overall prediction accuracy.

### Key Observations

1. **K-Nearest Neighbors (KNN):**
   - **Performance Consistency:** The KNN models (`KNN_1`, `KNN_2`, `KNN_3`) all demonstrate exceptional accuracy (0.998 or 0.996) and Weighted F1 Scores (0.998, 0.998, 0.996). This consistent performance underscores the effectiveness of KNN for anomaly detection tasks.
   - **Macro F1 Score Variability:** Despite high overall performance, the Macro F1 Scores for KNN models range from 0.902 to 0.915. This suggests that while KNN is excellent at overall prediction accuracy, it may face challenges with class imbalance, particularly in detecting minority classes.

2. **Support Vector Machines (SVM):**
   - **Kernel Impact:** The SVM models show a notable performance drop compared to KNN. `SVM_1` with a linear kernel achieved a Weighted F1 Score of 0.947 and an Accuracy of 0.954, while `SVM_2` with an RBF kernel showed a slight improvement, achieving a Weighted F1 Score of 0.96 and an Accuracy of 0.966.
   - **Macro F1 Score Challenge:** Both SVM models have significantly lower Macro F1 Scores (0.528 for linear kernel and 0.558 for RBF kernel), indicating that SVM may struggle with class imbalance, particularly in correctly identifying less frequent classes.

3. **Gradient Boosting (GBoost):**
   - **High Performance:** GBoost continues to demonstrate very high performance, with a Weighted F1 Score of 0.997 and Accuracy of 0.997. However, the Macro F1 Score (0.863) is lower than the other metrics, similar to KNN, indicating potential difficulties in handling minority classes effectively.
   - **Balanced Trade-off:** GBoost offers a strong balance between high accuracy and handling class distribution, making it a robust choice when accuracy is prioritized but some attention to minority classes is needed.

4. **Multi-Layer Perceptron (MLP):**
   - **Balanced and Improved Performance:** The MLP model achieved a Weighted F1 Score of 0.977 and an Accuracy of 0.978, which are both high, indicating strong overall performance. Its Macro F1 Score (0.696) is higher than that of SVM, suggesting better handling of class imbalances, although still lower than KNN and GBoost.
   - **Complexity and Flexibility:** The MLP configuration, involving multiple layers and tuning parameters (e.g., dropout, epochs, learning rate), demonstrates the potential of neural networks in achieving a balance between accuracy and handling class imbalance, albeit with more complexity.

# Conclusion

- **KNN as the Leading Performer:** KNN emerges as the top-performing model for this anomaly detection task, with the highest accuracy and Weighted F1 Scores across most configurations. However, the slight dip in Macro F1 Scores indicates that KNN may not be the best choice when the focus is on minority class detection.
  
- **SVM's Mixed Results:** SVM models, particularly with the RBF kernel, show decent accuracy but struggle significantly with class imbalance, as reflected in their low Macro F1 Scores. This makes SVM less ideal in scenarios where equal performance across all classes is critical.

- **GBoost for High Accuracy with Some Trade-offs:** GBoost is a strong alternative when high accuracy is the primary goal. However, it may require additional methods to enhance performance on minority classes, given its lower Macro F1 Score.

- **MLP for a Balanced Approach:** The MLP model offers a balanced and slightly improved approach compared to SVM, making it a good candidate when you need a reasonable trade-off between overall accuracy and class imbalance handling, though it may require more tuning and computational resources.

In a nut shell, the selection of a machine learning model for multi-class anomaly detection depends on the specific goals—whether the emphasis is on overall accuracy, the detection of minority classes, or the availability of resources for model tuning. **KNN** and **GBoost** stand out in terms of raw performance, while **MLP** offers a more balanced approach. **SVM**, though accurate, shows the need for careful consideration when dealing with class imbalances.

# Table 1:
| Index | Models | Feature Selection Methods | Configuration | F1 Score Weighted Avg | F1 Score Macro Avg | Accuracy |
|-------|--------|---------------------------|---------------|-----------------------|--------------------|----------|
| 0     | KNN_1  | Random_Forest              | k = 3, p = 2, metric = manhattan | 0.998                 | 0.915              | 0.998    |
| 1     | KNN_2  | Mutual Information         | k = 3, p = 2, metric = manhattan | 0.998                 | 0.914              | 0.998    |
| 2     | KNN_3  | RF                         | k = 3, p = 2, metric = manhattan | 0.996                 | 0.902              | 0.996    |
| 3     | SVM_1  | RF                         | kernel=Linear, regularization_term=l2, regularization_parameter=1.5, max_iter=1000, loss_function=hinge | 0.947 | 0.528 | 0.954 |
| 4     | SVM_2  | RF                         | kernel=rbf, degree=2, regularization_parameter=1 | 0.960                 | 0.558              | 0.966    |
| 5     | GBoost | RF                         | learning_rate=0.1, n_estimators=150 | 0.997               | 0.863              | 0.997    |
| 6     | MLP    | RF                         | no_neurons_1=64, no_neurons_2=128, no_neurons_3=128, dropout_rate=0.2, epoch=10, batch_size=32, learning_rate=0.0001, activation='relu' | 0.977 | 0.696 | 0.978 |


# **Split dataset**
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
</head>
<body>
    <img src="https://drive.google.com/uc?export=view&id=1zn-wpJgfOO6Pa_w-Kk35BgwNwwPm70gh" width="50%">
</body>
</html>
