# American-Sign-Language-Interpretation-Project
Building a machine learning model to recognize the ASL alphabet
# INSPIRATION BEHIND THE PROBLEM:
Sign languages across the world are different. There are 300 distinct sign languages across the world. Today, around one million people use 
American Sign Language (ASL) as their main way to communicate, according to Communication Service for the Deaf.
Our goal was to build a mobile application that uses a camera to capture a person signing the ASL alphabet, and translate it in real time. There are many other apps which require purchase with similar functionalities & our goal is to make our app available for everyone free of cost. This would involve:
- Gathering data
- Training a machine learning model to recognize the ASL alphabet
- Building the user interface.
# DATA COLLECTION:
During the dataset formation our team decided to create our own dataset, all the five members of our team added the images of the ASL alphabets in the Shared Google Drive folder which we named as ASL Library. We also supplemented our dataset with additional images from Kaggle and Google images. The total data set contains 5408 images where each alphabet folder contains close to 200 images. After the train test split of 80:20 the training dataset contains a total of 4326 images. And the test dataset contains 1082 images.
# CNN Model
The approach we took was to start with a more complex model in terms of the number of convolutions and filters, choice of optimizer, number and size hidden layers, and incrementally decreasing some of those values(if necessary) to find the right compromise between overfitting and underfitting to the data. A 3 x 3 filter size was used as standard throughout the filter layers. It seemed to gather enough detail from each image while not increasing the parameter number too high. We used the relu activation function for the convolutional and dense hidden layers because it is computationally efficient and allows the network to converge very quickly. The output dense layer used the softmax activation function because it can handle multiple classes well and normalized the outputs for each class between 0 and 1 and divides by their sum, giving the probability of the input value being in a specific class.
# Initial Models and Choosing the Right One
Gradient Descent was effective as an optimizer during some initial testing but could be painfully slow especially when running on our local computers/laptops. For the remainder of the models, we used Adam (adaptive moment estimation).For the scope of this project, we created a Machine Learning algorithm to be able
to identify each of the letters in an efficient and effective manner. Due to their proficiency with image classification and some preliminary testing, we used convolutional neural nets (CNN).During some preliminary testing, machine learning classifier models (MLP) and CNNs were runside by side on the same dataset with similar levels of complexity and the CNNs outperformed the MLPs by over 15% in most scenarios.
The typical structure of a CNN includes a layer (orlayers) of filter maps with the number of convolutional layers increasing (and oftentimes doubling)after each layer. This has been proven to be an effective method to acquire details and then subsequently put those details together to make and identify more structured “images”. To avoid overfitting and looking at other CNN models, we did not want to start with too high of a number of filters and started with 32.
# Results
The model was trained for a dataset size of 4326 images. The model was trained for 15 epochs.The initial training accuracy and validation accuracy increases drastically till the 8th epoch. The accuracy then attains a plateau limit as the epochs increase. The maximum validation accuracy attained is 90.33% at the 15th epoch. Whereas the maximum training accuracy attained is 98.03%.

