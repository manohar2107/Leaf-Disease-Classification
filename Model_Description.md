# Leaf-Disease-Classification
Deep Learning(CNN on Image Dataset)

Software/Hardware Requirement:
IDE:Anaconda,Jupyter Notebook(prefer Google Colab),Python 3.5 or above
Libraries:Keras,Tensorflow,Sklearn,OpenCv,numpy,matplotlib
Hardware Minimum req.:Intel Core i5 and above,GPU(>=2GB) is preferable(else leave system for 25 days open),4GB Internal Ram

Preprocessing Techniques(Segmentation,Augmentation) were essential for reducing overfitting and acquiring better accuracy.

Preprocessing:
Segmentation alone could not able to put maximum effect in feature extraction,so additional to that HSV masking(Thresholding),segmentation(morphological operation) and color feature extraction(Lab) in sequence gave better results.Code:Segmented in repository.

Training_Model:
As research paper suggested pre-trained AlexNet(accuracy of 78%), we used ResNet50 pre-trained on ImageNet(Approx 94 million real world dataset) giving us improved accuracy of 85.32%.
ResNet50 performs better than AlexNet,VGG16,InceptionV3 because in 2015 this model was published with solution of vanishing gradient(Skip Connection),and batch_normalization(increase stability and performance of model). We included 2 hidden layers of perceptrons(interconnected neurons) trained on different features.
After compiling above methods we used 1 more preprocessing technique augmentation(useful in small dataset,which in our case is 293 samples in dataset), helpful in reducing overfitting and hence using fit() function to fit dataset in our model.

Visualization:
So,result we obtained were pretty decent with 85.32% accuracy.
Code:Training_model in repository


Dataset Link:https://drive.google.com/drive/folders/1iC8kPsvpsgRPywQOMhUTkKbvIEX45PnR?usp=sharing
