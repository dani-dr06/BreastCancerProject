# Breast Cancer K Means Algorithm Project

Breast cancer is a big issue in women’s health. With a cancer’s stage being one of the biggest 
factors affecting a patient’s prognosis, early detection and treatment are crucial and can 
potentially lead to breast cancer going into remission. The purpose of this project is to carry out 
a k means algorithm in Python to analyze breast cancer data and predict the class of the patient 
(benign cells or malignant cells) based on 9 attributes: clump thickness, uniformity of cell size, 
uniformity of cell shape, marginal adhesion, single epithelial cell size, bare nuclei, bland 
chromatin, normal nucleoli, and mitoses.

## [Data Set](https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/breast-cancer-wisconsin.data)
The data comes from Dr. Wolberg’s Wisconsin Breast Cancer Data and a download is linked above.
The data set consists of 11 columns:

| ***Columns*** | ***Attributes*** | ***Names*** | ***Values*** |
| ------- | ---------- | ----- | ------ |
| 1 | Patient ID | Scn | Integer |
| 2 | Clump Thickness | A2 | 1 - 10 |
| 3 | Uniformity of Cell Size | A3 | 1 - 10 |
| 4 | Uniformity of Cell Shape | A4 | 1 - 10 |
| 5 | Marginal Adhesion | A5 | 1 - 10 |
| 6 | Single Epithelial Cell Size | A6 | 1 - 10 |
| 7 | Bare Nuclei | A7 | 1 - 10 |
| 8 | Bland Chromatin | A8 | 1 - 10 |
| 9 | Normal Nucleoli | A9 | 1 - 10 |
| 10 | Mitoses | A10 | 1 - 10 |
| 11 | Class | Class | 2 (benign) or 4 (malignant) |

## Project Parts
The project is divided into 3 parts.

<details><summary>Phase 1</summary>
<p>

Phase 1 of the project consists of obtaining the data and loading it in a Pandas dataframe, imputing 
missing values with the mean, and computing mean, median, standard deviation of each of the 
attributes, as well as drawing histograms for each of the attributes to have a better understanding of their distributions.

</p>
</details>

<details><summary>Phase 2</summary>
<p>

Phase 2 implements the k means algorithm. To begin, we randomly select two 
initial centroids and calculate the Euclidian distance from the two centroids for all data points. 
Each data point is then assigned to one of two clusters (2 for benign and 4 for 
malignant). Following the assignment to the two clusters, we recompute the two centroids by taking the mean of cluster 2 data points and cluster 4 
data points. These steps are repeated until one of two conditions is met: 
until the centroids do not change or the steps are iterated 50 times.

</p>
</details>

<details><summary>Phase 3</summary>
<p>

Here we analyze how well the clustering worked by calculating the individual and total 
error rates. To do so, we calculate the number of data points that were incorrectly predicted as 
class 2 when the correct class was 4, and vice versa, and divided by the number of class 2 data 
points and class 4 data points respectively. Finally, for the total error rate, we divide the total 
number of data points with predicted classes that do not equal the actual class by the total 
number of data points. Moreover, since the algorithm suffers from poor initialization, 
clusters are sometimes swapped; if the total error rate is greater than 50%, then the program 
swaps the predicted clusters and then calculates the error rates.

</p>
</details>

## Conclusion
Although the program has its flaws, like poor initialization for the k means algorithm, it
was still able to correctly classify a patient as either class 2 or class 4 96% of the time. Based on 
the 9 attributes (clump thickness, uniformity of cell size, uniformity of cell shape, marginal 
adhesion, single epithelial cell size, bare nuclei, bland chromatin, normal nucleoli, and mitoses), 
one can predict whether a particular patient’s tumor is benign or malignant, which could 
potentially save lives if the cancer is detected early enough and followed with the appropriate 
treatment.
