# Masked-Face-Recognition-NN

#Masked-Face recognition

#Team Members

-Tariq Hamdi
-Omar Abuhassan


#Introduction

These days after covid-19 has spread out, wearing masks is mandatory
to enter any organizations and institutions. Indeed, taking attendance
using fingerprints or regular schedules is risky and many companies are
looking for safe attendance and departure registration.Therefore, we will
try to build models that recognize people while they keep their masks on.


#Problem Description

Face recognition is the general task of identifying and verifying people
from photographs of their face.
To be more focused we just need face identification. Which is a
one-to-many mapping for a given face against a database of known
faces (e.g., who is this person?).
We used Masked_Unmasked_Mixed dataset, which contains:
- Train set: 69 persons with multiple masked and unmasked images
- Test set: same 69 persons but with just masked images


#Detailed Description

We searched for multiple solutions and we found that we must use CNN
since we are manipulating images.
First we used a simple classic CNN with a classification layer.
Unfortunately, the accuracy was low. so we tried to use some learned
models like VGG16 and we got a bit better results.
After that we tried to play on another scale. We used the CNN model just
for extracting the features from images then we fed it to another model
like RNN and the accuracy was improved.
Finally, after more searching we found an amazing model called
FaceNet which is a CNN model that needs previous training. It just
applies triplet-loss to do embedding, then we classify using SVM.
These our architectures:

1- Classic CNN


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/classic%20CNN.jpg?raw=true "Employee Data title")



2- Transfer Learning (VGG16)


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/Transfer%20learning.jpg?raw=true "Employee Data title")



3- CNN-RNN


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/CNN-RNN.jpg?raw=true "Employee Data title")



4- Facenet-SVM


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/FaceNet-SVM.jpg?raw=true "Employee Data title")

Experimental Results

1- Classic CNN


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/CNN%20Result.jpg?raw=true "Employee Data title")



2- Transfer Learning (VGG16)


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/Transfer%20learning%20Result.jpg?raw=true "Employee Data title")



3- CNN-RNN


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/CNN-RNN%20Result.jpg?raw=true "Employee Data title")



4- Facenet-SVM


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/FaceNet-SVM%20Result.jpg?raw=true "Employee Data title")


#Results Analysis

some of correct results:


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/CR1.jpg?raw=true "Employee Data title")

![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/CR2.jpg?raw=true "Employee Data title")



some of Incorrect results:


![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/ICR1.jpg?raw=true "Employee Data title")

![Employee data](https://github.com/Tariq-Hommadi/NN/blob/main/ICR2.jpg?raw=true "Employee Data title")

#Possible error sources:

- different color of the mask
- closed eyes
- Image with face from side
- wearing glasses


#Conclusion

As we show, the results of using different models will differ in the
accuracy obtained from the test set. The lowest accuracy that was
presented in our work is obtained from vanilla CNN (classic CNN) with a
test accuracy around 2.08%, and the best accuracy that we got was
around 50.595% that was obtained by implementing faceNet.


#References
- Masked_Unmasked_Mixed dataset: Masked_Unmasked_Mixed |
Kaggle
- FaceNet Model: https://www.kaggle.com/nikhil1011/facenet
