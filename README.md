<h1 align="center">  SC1015_Project : <br/> Detection of Pneumonia using X-rays </h1><br/>

## What is Pneumonia?
<img width=50% alt="image" src="https://www.h-h-c.com/wp-content/uploads/2021/08/Lobar-Pneumonia.png">
Pneumonia is an infection that inflames the air sacs in both lungs. It is one of the leading causes of death in Singapore and worldwide. Accounting for 20.7%, 18.8% and 18.4% of deaths in Singapore in 2019,2020 and 2021 according to the death statistics retrieve from HealthHub. As for worldwide, statistics has shown that 2.5 million people have died from pneumonia in 2019.<br/>

## Problem Statement
**How might we detect pneumonia for doctors in order to increase the effeciency and accuracy of diagnosis?** <br/><br/>
As normal examination and detection of pneumonia takes a period of time and requires human supervision. We decided to use machine learning to find a way to help to increase the efficiency, reduce the amount of manpower needed and improve diagnostic accuracy for pneumonia. 
<br/>

## Dataset
<img  width=50% alt="image" src="https://i.imgur.com/jZqpV51.png">
<br/>
The dataset that we have picked is <b>Chest X-Ray Images (Pneumonia)</b> (Kaggle link: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
<br><br>
The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).
<br><br>
All Chest X-ray images were select from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. 

<br/>

## Convolutional Neural Networks (CNN)
<br/>
<img width=50% alt="image" src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*vkQ0hXDaQv57sALXAJquxA.jpeg">
<br>
Within deep learning, CNN is a type of neural network that are specifically designed for processing data that has a grid-like structure, such as images, video, and audio. The network extracts relevant features from input images through convolutional and pooling layers, followed by fully connected layers that classify the image into categories.
<br/><br/>
In our project we have used CNN on the x-ray images of patients to classify if the patient has pneumonia or not. 

## Densely Connected Convolutional Network (DenseNet)
<br/>
<img width=50% alt="image" src="https://pytorch.org/assets/images/densenet1.png">
<br>
DenseNet is a type of deep neural network architecture that is designed to address the vanishing gradient problem in very deep neural networks. DenseNet models consist of densely connected blocks of layers, where each layer is connected to every other layer in a feed-forward fashion. This design enables each layer to receive information not only from the preceding layer but also from all the preceding layers in the network.
<br/><br/>
In our project we have chosen to used DenseNet121 to do a basic comparison between the state-of-the-art CNN architecture and the primitive implementation of a basic CNN.
<br/>

## Conclusion 
#### Best Performance model: DenseNet121
The DenseNet121 model performed the best with an 80.1% test accuracy and a loss of 0.987, outperforming a primitive CNN model. DenseNet models have more layers and are more complex, addressing the vanishing gradient problem and learning complex representations through shortcut connections between layers. The CNN model achieved a 96.6% training accuracy and 79.0% testing accuracy, while the DenseNet model achieved 98.5% training accuracy and 80.1% test accuracy.

#### Solution to Problem Statement
Using the DenseNet model to detect surface-level symptoms would serve as a fundamental tool for medical professionals to speed up their diagnosis. The project has inspired the potential for technology to revolutionize the end-to-end process of diagnosis and treatment plans with the help of AI models and tools.
<br/>

## Lesson learnt 
#### Technical 
There is a limit to the number of layers you can stack before the performance of the model starts to drop due to vanishing gradients and overfitting <br/>

#### Ethical Concerns
Worth mentioning that even if a model is highly performant and accurate, utilising it in an unethical way can lead to adverse outcomes. Decision still  ultimately lies with the doctors and this can only serve as a tool to assist <br/>

#### Data Analysis
The use of images to analyse the data is quite challenging due to its limitation, hence, exploring the data through techniques such as pixel intensity can help in finding features to help us in tuning the data <br/>

#### Resources
Given the constraints of resource and time, we had to scale down the input pixel size. Using a larger input pixel size could result in a better performing model <br/>


## References 
Mooney, P. (2018, March 24). Chest X-ray images (pneumonia). Kaggle. Retrieved April 14, 2023, from https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia 

Saha, S. (2022, November 16). A comprehensive guide to Convolutional Neural Networks - the eli5 way. Medium. Retrieved April 12, 2023, from https://towardsdatascience.com/a-comprehensive-guide-to-convolutional-neural-networks-the-eli5-way-3bd2b1164a53 

Pytorch. PyTorch. (n.d.). Retrieved April 12, 2023, from https://pytorch.org/hub/pytorch_vision_densenet/ 

Basic classification: Classify images of clothing &nbsp;: &nbsp; Tensorflow Core. TensorFlow. (n.d.). Retrieved April 13, 2023, from https://www.tensorflow.org/tutorials/keras/classification 
