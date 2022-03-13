# Credit Risk Analysis
## Project Overview
In this project, I utilized Python to build and evaluate machine learning models to predict credit risk. 
Below are the following procedures:
- Oversampling the data using the RandomOverSampler and SMOTE algorithm
- Undersampling the data using the ClusterCentroids algorithm
- Using a combinatin approach of over and undersampling using the SMOTEENN algorithm
- Comparing the two machine learning models to reduce bias. Using BalancedRandomForestClassifier and EasyEnsemble Classifier

From these procedures that we followed, we can determine whether or not to use these models to predict credit risk. 

# Results
## RandomOverSamplerModel

Random oversampling

![RandomOverSampler](https://user-images.githubusercontent.com/91761603/158074395-c6654ae1-5c8c-44b5-be2d-738f9bf94aea.png)

The balanced accuracy score is 65%.

![PredictedHighRisk](https://user-images.githubusercontent.com/91761603/158074455-9452d27f-ec5c-4703-be50-5b1c1f22adc9.png)
![Screen Shot 2022-03-13 at 11 46 13 AM](https://user-images.githubusercontent.com/91761603/158074506-76c0cdb7-eacc-49a0-9694-70a9211fd9fc.png)

The high risk precision is 1% with 62% sensitivity.
Due to the high number of the low risk population, the precision is very close to 100% with a sensitivity of 68%.

## SMOTE model-
Oversampling technique where teh minority class is increased. 

![Screen Shot 2022-03-13 at 11 49 25 AM](https://user-images.githubusercontent.com/91761603/158074604-0d4db409-b8a8-4949-b1e8-5be14507b7ab.png)

Compared to our previous model, the balanced accuracy score is relatively the same at 64%.

![Screen Shot 2022-03-13 at 11 50 37 AM](https://user-images.githubusercontent.com/91761603/158074648-5918fbc4-39a1-40e3-997f-247b26f6ced4.png)
![Screen Shot 2022-03-13 at 11 50 54 AM](https://user-images.githubusercontent.com/91761603/158074654-03a0b204-4a7b-488a-8731-9c9f13e816c7.png)

The results from the SMOTE model is very similar to our previous model. 
Both balanced accuracy score is 64%. There is a 2% difference when we compare the sensitivity level. The previous model with a sensitivity level of 68% and the current at 66%.

## ClusterCentroid Model
![Screen Shot 2022-03-13 at 11 53 32 AM](https://user-images.githubusercontent.com/91761603/158074727-b5a87946-f926-4812-a859-db344fdd9c0e.png)
![Screen Shot 2022-03-13 at 11 55 55 AM](https://user-images.githubusercontent.com/91761603/158074806-2a10d3a5-629d-4b10-bd5d-c2a1a7358518.png)

With the ClusterCentroid model, our balanced accuracy score went down from the previous model at 64% to 52%.
The high risk precision is at 1% with 63% sensitivity. Low risk sensitivity is only at 40%.

## SMOTEENN Model
![Screen Shot 2022-03-13 at 11 58 12 AM](https://user-images.githubusercontent.com/91761603/158074871-c9b79de6-e1e8-49b3-9eab-161d17803690.png)
![Screen Shot 2022-03-13 at 11 58 47 AM](https://user-images.githubusercontent.com/91761603/158074886-35cfdcce-cd11-46be-be2d-54da77f7c9e4.png)
![Screen Shot 2022-03-13 at 11 59 03 AM](https://user-images.githubusercontent.com/91761603/158074894-0bf91151-4d72-40c8-a545-d23c0a092e8f.png)

The balanced accuracy comes out to be around 62%. 
The high risk precision is stagnant at 1% with a 68% sensitivity and due to the hgih number of false positives, the low risk sensitivity is at 57%. 

## BalancedRandomForestClassifier Model 
![Screen Shot 2022-03-13 at 12 05 18 PM](https://user-images.githubusercontent.com/91761603/158075056-ca10e965-a0f3-4071-b7c2-ff52f4655d6b.png)
![Screen Shot 2022-03-13 at 12 05 49 PM](https://user-images.githubusercontent.com/91761603/158075073-bccb23e4-91d9-4e82-9a97-8b8df4585be1.png)
![Screen Shot 2022-03-13 at 12 06 42 PM](https://user-images.githubusercontent.com/91761603/158075091-c01a471d-5050-486a-8fb2-9f00724cde38.png)

The balanced accuracy with this model positively increased to 79% compared to the other models we've utilized. The high risk precision is at 4% wiith 67% sensitivity. With a lower number of false positives, the low risk sensitivity is now at 91% with precision of 100%. 

## EasyEnsembleClassifier Model
![Screen Shot 2022-03-13 at 12 09 22 PM](https://user-images.githubusercontent.com/91761603/158075188-89eb2d27-4fb1-4dbd-8b9d-30b8f84947af.png)
![Screen Shot 2022-03-13 at 12 09 33 PM](https://user-images.githubusercontent.com/91761603/158075198-2bf516c3-a7fa-4374-bb08-ef33c1d18f70.png)
![Screen Shot 2022-03-13 at 12 09 45 PM](https://user-images.githubusercontent.com/91761603/158075201-526a2c2e-d353-4dda-a90c-17b8fedc2881.png)

With the EasyEnsembleClassifier model, our balanced accuracy score is at 93%. The high risk precision is a little higher at 7% compared to our previous models with a 91% sensitivity. With a lower number of false positives, the lower risk sensitivity is now at 94% with 100% precision. 

# Summary
Out of the five models we've utilized for credit risk analysis, we can conclude that the last model, the EasyEnsembleClassifier model would be the best model to use. It shows a recall of 93% which captures most of all high risk credit. This model has the best accuracy but would still air on the cautious side as it might be prone to overfitting. One issue with this model from our results, indicates a large number of false positives, meanining that large number of low risk loans were marked as high risk.

