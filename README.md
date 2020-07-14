# Style Transfer with Deep Neural Networks

In this notebook, I have *recreated* a style transfer method that is outlined in the paper,
[Image Style Transfer Using Convolutional Neural Networks, by Gatys](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) in PyTorch.

Style transfer uses the features found in the 19-layer VGG Network, which is comprised of a series of convolutional and pooling layers, and a few fully-connected layers. In the image below, the convolutional layers are named by stack and their order in the stack. Conv_1_1 is the first convolutional layer that an image is passed through, in the first stack. Conv_2_1 is the first convolutional layer in the second stack. The deepest convolutional layer in the network is conv_5_4.

<img src='https://miro.medium.com/max/875/0*5uxP_d6UTy6NlHAU' width=80%/>

In this notebook, I have used a pre-trained VGG19 Net to extract content or style features from a passed in image. I have then formalized the idea of content and style _losses_ and used those to iteratively update the target image until we get the result.

Style transfer relies on separating the content and style of an image. Given one content image and one style image, we aim to create a new, target image which should contain our desired content and style components:
  * objects and their arrangement are similar to that of the **content image**
  * style, colors, and textures are similar to that of the **style image**
  
![git](https://user-images.githubusercontent.com/53137708/87464534-e4f1c080-c630-11ea-8dd4-d3c9cc30dcb7.png)

In the above image some of the features are lost but we can get exteremly good results by using the state of the art networks, for example [Deep Dream Generator](https://deepdreamgenerator.com/) uses the same principle and can generate some great art shown below.


 <img src='https://user-images.githubusercontent.com/53137708/87465331-1323d000-c632-11ea-9d4a-7fe1319bda3f.jpg' width="250" height="250"/>


The Images/Dataset used in this notebook is hosted here [Style Transfer Dataset](https://www.kaggle.com/anuranjan5/style-transfer-images)
