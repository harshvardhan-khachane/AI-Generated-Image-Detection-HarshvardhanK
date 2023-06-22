# AI-Generated-Image-Detection-HarshvardhanK

*Brief problem statement:*

Hi! This project was created for the bitgrit competition for "Generative AI" (https://bitgrit.net/competition/18#). We must categorise the photos as real (label '0') or artificially created (label '1'). The datasets contain just 20 × 20 x 3 (channels) sized photos. Since the underlying information has already been altered, it cannot be changed back to the original images. The objective of this challenge is to forecast the 'labels' column using the supplied data.

**Classifiers and techniques used**
1. *PCA(*Principal Component Analysis)
2. *Naive Bayes Classifier*
3. *Softmax Classifier*
4. *Support Vector Classifier*
5. *Adaboost*
6. *GradBoosting*
7. *Random Forest*
8. *Voting Classifier*


## Procedure
1. After loading the data, preprocessed it by changing all features in the range of 0 to 1 using the *MinMaxScaler*.
2. Divide the test and train sets of the training data (1:4).
3. 3 different classifiers were applied to the data, and the accuracy was evaluated.

   1)  *Naive Bayes Classifier*:
   The accuracy was *62.1904761904762%*
   ![Pic 1](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/714b3623-234c-4810-b454-15a7b8874f6e)




   2)  *Softmax Classifier*
   The accuracy was *80.85714285714286%*
   ![pic2](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/f9ec6548-df6d-4b02-a086-efd78e714c9e)



   3)  *Support Vector Classifier*(with linear kernel)
   The accuracy was *80.95238095238095%*
   ![pic3](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/dfce08a3-4acf-4084-bc16-b8204f4ab4e1)




4. Following that, I proceeded to apply Principal Component Analysis (PCA) to the data and evaluated its accuracy using the aforementioned classifiers.The outcome of this analysis is as follows:
5. 
   ![pic4](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/cf4f2d6f-dfe6-4d1d-9afe-ff1b44baf173)




   ![pic5](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/93dca6ed-f683-4a4e-af5a-2576b4c379f4)
   



6. The Support Vector Classifier (SVC) demonstrated the most favourable outcomes, displaying the highest performance among the classifiers used. Through meticulous adjustment of the number of components, it was determined that when set to 208, the Linear Kernel achieved a prediction accuracy of *86.47619047619047%*.
7. 
   ![pic6](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/84be97f7-3029-4174-a488-5783be9b3f95)


8. PCA+SVC Linear performed pretty well, with a f1 score of *0.7968* .
9. Subsequently, I explored more advanced techniques such as bagging, boosting, and other methods in an attempt to enhance the accuracy even further.
10. Initially, I employed the Bagging technique, which resulted in an f1 score of *0.85588235*.
   ![pic7](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/9a46b6d5-96f2-4139-9b40-8fb61c596d5c)


11. Next, I experimented with GradBoosting. However, when using lower learning rates, the accuracy did not meet expectations. On the other hand, when using higher learning rates, the model demonstrated overfitting, with the validation set showing significantly poorer accuracy compared to the testing set. Consequently, I decided not to include this approach in the final submission.
   ![pic8](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/96b7aa0c-ae87-44f5-8097-f186f6e83dcd)


12. Lastly, I employed AdaBoosting with SVC as the base classifier, considering its superior accuracy from previous attempts. Notably, this approach yielded the highest accuracy thus far, achieving an f1 score of 0.87572254.
  ![pic9](https://github.com/harshvardhan-khachane/AI-Generated-Image-Detection-HarshvardhanK/assets/99604231/eae91c92-45e9-4fe1-9c89-4f50a9464725)
