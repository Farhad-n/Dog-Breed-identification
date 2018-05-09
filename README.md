# Dog-Breed-Identification
The goal of this analysis is to identify the various breed of dogs using Dog images provided in kaggle data set. 

This document is intended to go through the entire process step by step and at each step talk about the challenges faced during this project. 
* **Steps:**
1. Initiate Google Drive feature in Colab utilize cloud computing power
 * Discuss the Colab Feature to upload the data.
 * Discuss the alternative approaches.
2. Obtaining images. 
3. Preprocess the images. 
4. Create training data set X_train, y_train 
5. Create the X_test dataset
6. Prepare data to fit into a deep learning model
7. Build Model (Few Models are considered)
 * Simple CNN (Convolutional Neural Network)
 * Sequential CNN VGG style with 2 VGG block inception module architecture
 * Functional API CNN with inception architecture using BatchNormalization and Dropout
 
The Best Model will be selected to test against the test data.
A commentary for each step will be provided along with some visualization and summary through the process.  
in conclusion a summary commentary will be provided to discuss the challenges, weaknesses and opportunities for improvement in the models or the process.  
## Conclusion
The interesting point of this particular project was training set data.  there were total of 10222 dogs in the taring directory and 120 unique dog species. the histogram of this data set showed and average of 100 dogs per breed category.  this is too small of data.  The 3 model utilized in here are the basic one CNN, one two segment VGG and the third one is functional API model with inception module.  The best validation accuracy was with functional API at about 10% very low. the result does indicate a major overfilling in these models.  
**Following are some ideas for reducing overfitting:**
* Add more data
 * This was not possible limited by data set.  
* Use data augmentation
 * This is the most promising way to help this problem which requieres abit more work to add to this data set. 
* Use architectures that generalize well
* Add regularization (i.e dropout)
 * Various dropout was utilized and the best one was picked for each model
* Reduce architecture complexity. 
 * tried removing some layers but not much help in here.
 
**I was able to increase the validation accuracy form couple of percent to about 18% the high-water mark. Next, I will try the input augmentation to see the improvement on the prediction.  This will require a bit of work.**  
