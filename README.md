# CPSC-599-Final-Project

### What is this project about?
The main goal/objectives of our project is to create a model that learn through several processing layers that break down complex images into series of simple mappings so that it can learn the difference between the images feeded to it to discriminate into either malignant or benign kinds of cancer (specifically lung cancer).


### About the dataset
We got the dataset from a grand challenge website. (https://wsss4luad.grand-challenge.org/)

Only images with one of the following labels are included: normal, stroma or tumor.

Distribution of the data:

![Data Distribution Chart](https://github.com/lybned/CPSC-599-Final-Project/blob/main/images/chart.png?raw=true)


### Preprocessing

All the labelled data are split into 3 different sets: training (60%), validation (20%) and test (20%) sets.
We also create a weighted sampler based on the distribution of the labels so that labels with low occurrence will get more chance of being picked. The weight for each label is calculated by 1/<Total number of the occurrence>. 

### Data Augmentation
50% for a horizontal flip
resize the image to (232px, 232px)
random crop of an image of 224p
convert the image to tensor
50% for normalizing the pixel color to a mean of [0.485, 0.456, 0.406] with a standard deviation of [0.229, 0.224, 0.225].


### Model and Frameworks

Model: ResNet-50 from Pytorch. We froze the everything in the first layer.

Frameworks: Pytorch


### Training Procedure

![Data Distribution Chart](https://github.com/lybned/CPSC-599-Final-Project/blob/main/images/Flowchart.png?raw=true)

### Final Results



#### Training Loss and Accuracy
![Data Distribution Chart](https://github.com/MohammadSoomro/CPSC_599_PROJECT/blob/main/images/Graph%20Image.png?raw=true)


#### Validation Loss and Accuracy
![Data Distribution Chart](https://github.com/MohammadSoomro/CPSC_599_PROJECT/blob/main/images/Graph%20image%202.png?raw=true)


#### Results for the final best model on the test set:
● Validation accuracy = 96.70%
● Loss = 0.085
● Sensitivity = 97.12%
● Specificity = 98.26%
● Precision = 96.74%

