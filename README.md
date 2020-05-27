# Image Segmentation and Medical Imaging using U-Net to Find Nuclei in Divergent Image

Semantic Segmentation is to classify every single pixel on the image as belonging to a specific class (rather than objects as in classification tasks)

To bring about this, a CNN encoder-decoder network called U-NET is adopted.

![Convolutional-neural-network-CNN-architecture-based-on-UNET-Ronneberger-et-al](https://user-images.githubusercontent.com/51057490/83078413-7a30f980-a071-11ea-8ed3-a14b17b16d0e.png)
                                                
The input to the U-NET is an image and the output is a segmentation map (a binary mask of the input image)

A binary image consists of an image that has a color code of either 255 (white) or 0 (black), hence it outputs white for the area of interest (foreground) and black for the background which leads to the semantic segmentation

The idea of this project is to spot nuclei to speed up curing process for every disease - by automating nucleus detcetion, you could help unlock cures faster. 

The aim is to create an algorithm to automate nucleus detection so that researchers can identify each individual cell in a sample, 
and by measuring how cells react to various treatments, the researcher can understand the underlying biological processes at work. 
![dsb](https://user-images.githubusercontent.com/51057490/83078426-81580780-a071-11ea-8340-8b50e34aa03a.jpg)

I tackled this problem by using the U-NET for producing the segmentation map.

*The Workflow for this kernel includes:*

- Load the dataset from Kaggle
- Build an Input Data pipeline that does some image preprocessing and also stacks together multiple masks corresponding to a specific image
- Configure a custom IOU metrics (IOU of segmentation is clearly different from IOU of object detection but same underlying intuition)
- Build a U-NET architecture that returns a binary mask of the input image
- Train the Model using Keras Callbacks - EarlyStopping & ModelCheckpoint
- Test the trained model on unseen data and Plot the results using Matplotlib

Here are the results:


![rq4](https://user-images.githubusercontent.com/51057490/83079101-fb3cc080-a072-11ea-9f1e-b69c79d26d78.JPG)
![rq3](https://user-images.githubusercontent.com/51057490/83079105-fd9f1a80-a072-11ea-8b26-84e7f3a8302e.JPG)
![rq2](https://user-images.githubusercontent.com/51057490/83079113-042d9200-a073-11ea-89ed-39ce8ebb5406.JPG)
![rq1](https://user-images.githubusercontent.com/51057490/83079118-07288280-a073-11ea-9676-df8c24109efc.JPG)
