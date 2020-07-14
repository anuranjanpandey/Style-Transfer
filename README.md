# Style Transfer with Deep Neural Networks

In this notebook, I have *recreated* a style transfer method that is outlined in the paper,
[Image Style Transfer Using Convolutional Neural Networks, by Gatys](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) in PyTorch.

In this notebook, I have used a pre-trained VGG19 Net to extract content or style features from a passed in image. I have then formalized the idea of content and style _losses_ and used those to iteratively update the target image until we get the result.
