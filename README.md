# Multiclass classification model development using a custom convolutional neural network in TensorFlow to accurately detect Melanoma.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- # Background of the project :   
- Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. 
- # Problem being solved :  
- The purpose of the project is to develop a CNN based model which can accurately classify the input images into appropriate skin cancer type. Model is trained to classify total 9 types of skin cancer. The special interest is to be able to detect Melanoma which is one of the deadliest cancer type. 
- # Dataset being used :  
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC. Data belongs to total 9 classes each representing a type of cancer. 



## Conclusions
- # Models built :
- Total 3 models were built to solve the problem. Each model consists of 15 weight layers. However, 1st model did not have any drop-out layer, normalization layer, augmentation strategy. Also, it was trained on original data which had significant class imbalance. 2nd model had drop-out layers incoroporated. Also, augmentation strategy of randomflip and random rotation were used. It was also trained on original data which had significant class imbalance. 3rd model also had batch normalization incoporated in addition to drop-out layer. Also, class imbalance was removed by adding 500 images of each class using augmentor package.  
- # Comparison of Models :
- 1st and 2nd model had very low training as well as validation accuracy indicating underfitting. However, 3rd model gave satisfactory performance with training accuracy of more than 85%. Also, for 3rd model validation accuracy closely following training accuracy indicating not much overfitting. 
- # Possible reason for difference in performance of model :  
- The third model was trained on data where classes were balanced by adding 500 images to each class by using augmentor package. Also, batch normalization was used. Either of the two or both of these factors seem to have contributed to significant improvement in model performance. 


## Technologies Used
- Augmentor version 0.2.12
- keras     version 2.12.0
- pathlib   version 1.0.1
- tensorflow version 2.12.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- We thank Upgrad for introducing the problem statement to us as a part of an assignment. 



## Contact
Created by Yashodhan[@yashodhansg], Shailesh, Vidhyasaghar - feel free to contact us!



