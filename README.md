## Classification of images into 75 different classes     
      
### Summary     
      
#### Links    
    
[Project proposal](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Analysis%20report.pdf)      
[jupyter notebook part 1](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/P1_GettingDataReady.ipynb)     
[jupyter notebook part 2](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/P2_VisualizationEDA.ipynb)         [jupyter notebook part 3](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/P3_ConvNet.ipynb)        
[Slide deck](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Slide%20Deck.pptx)         
[Data](https://www.kaggle.com/moltean/fruits)
        
**Problem:**         
        
![Problem](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/Problem.PNG)
         
**Potential Clients:**    
        
Mobile applications that track calorie intake. Instead of manually entering the number of calories, users of such applications can just take a picture of the fruit that they are consuming and calories associated with that specific fruit can automatically be added. This will be a major attraction for users of such as applications.        
              
One item that most if not all major grocery markets carry are fruits. An application which can sort fruits automatically will be of great benefit for these markets. In a larger context, this will be a first step in developing an application that can recognize a wide range of items carried by these stores.
            
**Data type:** Around 50,000 RGB images in .jpg format. 
     
**Target variable:** 75 different fruit classes.   
       
**Features:** Pixel values (converted to 3D tensors).   
      
**Methodology and results**
      
1- [**Data wrangling:**](https://www.kaggle.com/rehanali88/kaggle-for-deep-learning-p-1-getting-data-ready) Check that every folder has the same number and identity of class. Check that no folder is empty. Split the dataset into training, testing and validation dataset. [Download split datasets](https://www.kaggle.com/kernels/svzip/4423114)       
          
![Splitting](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/DataSplitting.PNG)          
       
2- [**Exploratory analysis:**](https://www.kaggle.com/rehanali88/kaggle-for-deep-learning-p-2-visualization-eda)         
             
Different classes of fruits:        

![AllFruits](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/fruits.png)   
                       
![Widget](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/iWidget.png)             
       
Number of images in different classes:     
      
![TrainingNumber](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/trainingSet.png)      
![ValidationNumber](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/validationSet.png)       
![TestNumber](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/testSet.png)        
       
Insights from the plots:           
       
1- There are approximately 500 images for each class in training set.      
2- There are approximately 125 images for each class in validation set.       
3- There are approximately 50 images for each class in the test set.        
          
**There is no class imbalance. Excluding only a few classes, the number of fruits in all the classes is equivalent.**
      
Other insights from the data:     
       
Number of training images = 37836             Batch size = 18     
Number of validation images = 9554            Batch size = 17
Number of test images = 3155      
Number of classes = 75             
          
Steps per epoch is calculated by using the following formula:         
         
Steps per epoch = Total number of images / Batch size         
          
[Download CNN parameters csv file](https://www.kaggle.com/kernels/svzip/4504282)        
             
3- [**Convolution neural network:**](https://www.kaggle.com/rehanali88/kaggle-for-deep-learning-p-3-conv-net)       
        
 [Model 1:](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/tree/master/Model%201)          
         
![Architecturel](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/Architecture.PNG)      
          
Evaluation:         
         
![Model1](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/Model1.png)         
          
1.	Validation loss shows a slight but steady increase as epoch number increases along with high variability.          
2.	Validation loss and accuracy never reach the values close to training loss and accuracy.            
3.	We might be overfitting the data.       
            
[Model 2:](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/tree/master/Model%202)           
           
Addition 1: Addition of a dropout layer to randomly remove half the values from the previous layer. This prevents the model from learning random noise in the data.          
           
Addition 2: Data augmentation. Increasing variablilty by transforming training images.            
           
![Augmentation:](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/Orange.png)          
            
Evaluation:         
          
![Model2](https://github.com/rali88/Capstone-Fruit-classification-using-ConvNet/blob/master/Images/Model1%2B2.png)
            
1.	Validation loss does not increase as epoch number increases.          
2.	Validation loss and accuracy reach values close to training loss and accuracy.            
3.	We are not overfitting the data.               
