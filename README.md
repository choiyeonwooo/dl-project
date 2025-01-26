## MobileNet and 4 transformations.   
Image Classification based on CNN has developed with models VGG, ResNet, NesNeXt, Efficient Net, ... by reducing no. of parameters and training time and increasing accuracy.    
This project focuses on implementing image classification based on MobileNet, which has less parameters and training time but high accuracy.   
   
Below shows MobileNet body structure.   
<img width="234" alt="image" src="https://github.com/user-attachments/assets/6f92a7b6-c911-47c3-9545-99cde762c77b" />
***      
### Dataset
CIFAR-10   
10 label, 50000 trainset, 10000 testset   
***   
### Model Transformations
Based on MobileNet, I made some changes.   
Model1: skip connection added after every depthwise, pointwise convolution pair.   
Model2: skip connection added after every convolution layer.    
Model3: divide some convolution layers to other groups to enhance cardinality.   
Model4: replace initial convolution layer with grouped convolution and add channel shuffle.   

Below table shows result of 4 different versions of model      
![image](https://github.com/user-attachments/assets/98820d85-c3f3-4457-801b-d6607f56ed4d)
