# Project proposal  
   
## Classification of fruit images using  deep learning  
   
### The problem and potential clients   
   
Image classification is increasingly being used in mobile applications. An example where classification of fruits will be helpful are applications which are used to track calorie intake. The first target of this project will be such mobile applications:
   
**Mobile applications that track calorie intake. Instead of manually entering the number of calories, users of such applications can      just take a picture of the fruit that they are consuming and calories associated with that specific fruit can automatically be added. This will be a major attraction for users of such as application.**   
       
Another example where fruit classification can be helpful is the identification of grocery items in a grocery store. Sorting of these items and placing them in their respective aisles is a problem that can be automated with applications that can identify these items. The second target of this project will be such stores:   

**One item that most if not all major grocery markets carry are fruits. An application which can sort fruits automatically will be of great benefit for these markets. In a larger context, this will be a first step in developing an application that can recognize a wide range of items carried by these stores.**   
       
Apart from this specific project of classifying fruit images, image classification has applications across a wide range of businesses. From photo organization mobile applications to facial recognition used by social networking websites, image classification is being used to enhance business value and/or user experience. For example, identifying the type of damage a car has undergone can inform an insurance company about a potential claim and help them make an informed decision.   
   
In summary, the skills required for image classification have a wide range of applicability. Therefore, an understanding of the process of image classification is crucial for any data scientist.   
   
### Data: What it is and how will it be acquired   
   
The data for this analysis will be images of more than 60 different fruits. This will be acquired from the following data base link:
https://www.kaggle.com/moltean/fruits/data   

   
### Approach outline   
   
This classification will be performed using deep learning. As this will require a Graphical Processing Unit (GPU), the analysis will be performed using Kaggle’s GPU. The project will be divided into three parts.   
   
#### Part-1: Data wrangling   
   
We will gather some important information about the data set. This will include the number of classes and the number of images in each class. More importantly, as the data does not have a test set, the validation set will be split in the following way: 25 % of randomly picked images from this set will be moved in to the newly created test set, while the remaining will be kept in the validation set. All the data sets (training, testing and validation will be saved and will be used in the second part of the project.  We will also make sure that different sets have the same classes.   
   
#### Part-2: Build a simple convolution neural network   
   
We will use the split data sets from part 1 to build a simple convolution neural network. The network will be composed of layers of convolution and max pooling layers followed by a flatten and two densely connected layers. The validation and training loss and accuracy will be plotted as a function of epoch number to check for over fitting. Finally, the model will be evaluated on the test data set.   
   
#### Part-3: Build a convolution neural network with a drop out layer and data augmentation   
   
If the simple convolution neural network shows over fitting, then a new network with a drop out layer will be added to the network. Also, the training data will be augmented by randomly transforming training images so that the network does not see the image twice. As in part 2, plots of accuracy and loss will be used to test for over fitting and the model will be evaluated on the test data set.   
   
### Deliverable   
   
   1. The different notebooks each for the different parts of the project:   
       
      • [Notebook in which data manipulation and data splitting is performed.](https://github.com/rali88/Capstone-Project-2/blob/master/Getting%20data%20ready-kaggle%20Part-1.ipynb)      
      • [Notebook in which a simple convolution neural network is built and tested.](https://github.com/rali88/Capstone-Project-2/blob/master/Simple-ConvNet-P-2.ipynb)   
      • [Notebook in which convolution neural network with a drop out layer and data augmentation is built and tested.](https://github.com/rali88/Capstone-Project-2/blob/master/ConvNet-with-augmentation-P-3.ipynb)         
       
   2. A complete report outlying the need for the analysis, the approach taken and the results obtained.    
   3. A slide deck defining the problem, approach and the results obtained.

