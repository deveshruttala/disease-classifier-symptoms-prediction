# Disease-classifier and symptoms-prediction
This project completely  consists of me creating notebook on disease predictions, symptoms analysis, disease classifications <br>
This documentation outlines the implementation of disease prediction from symptoms using various ML models for heart disease, Alzheimer's, and other diseases. Employing SVM, KNN, Naive Bayes, Decision Tree, Logistic Regression, and more, our approach aims to enhance predictive accuracy, aiding early diagnosis and effective healthcare interventions.


<br><br>
<p align="center">
 <img height=200px src="readme assets/disease prediction asset.png" alt="Disease-Prediction">
</p>

<h1 align="center">Disease Prediction from Symptoms , heart disease classification and prediction </h1>


<br><br>


### Requirements
1. Python 3
2. sci-kit-learn
3. matplotlib
4. seaborn
5. numpy
6. pandas

### Process

- `Data extraction and cleaning` :  Basic cleaning, segmentation of columns and string formatting were performed in Excel. 
- `Data preprocessing` : Data preprocessing tasks performed include:
  * Spelling mistakes in the names of diseases or symptoms or their codes was rectified
  * The codes which were given to diseases and symptoms were removed as they were irrelevant for our task
  * A cumulative list of all symptoms was made 
  * Each symptom was assigned a Boolean value of 0 or 1 for each disease, according to whether the symptom occurs with the disease or not
- `Data visualization` : Built correlation heatmaps for the relationship between the symptoms and relationship between the diseases
- `Model Building` : Used 2 algorithms for this dataset and compared the results to evaluate which one yielded better results: *Multinomial Naive Bayes Classifier* and then  used KNN and SVM to check our  accuracy 
<br><br>

<h3 align="center">Implementation Process of Disease prediction  </h1>

<p align="center">
 <img height=200px src="readme assets/implementation.png" alt="implementation">
</p>

<br><br>

* For trying out git clone this project and the notebooks are self-explanatory  

```
git clone https://github.com/deveshruttala/disease-classifier-symptoms-prediction.git
```

#### Conclusion and credits

In conclusion, the implementation of disease prediction using diverse machine learning models, including SVM, KNN, Naive Bayes, Decision Tree, Logistic Regression, and more, exhibits promising results. These models contribute to enhanced healthcare decision-making.And I would like to extend my  for this report go to the dedicated efforts of the research member and who guided me in making this project 





